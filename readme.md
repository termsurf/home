<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h3 align='center'>@termsurf/home</h3>
<p align='center'>
  TermSurf Home Base
</p>

<br/>
<br/>
<br/>

## Introduction

This is the entrypoint into the team shared repos. See and run the `./load.sh` script to install all the public and private repos when you first get started.

- We have 1 API under `base.surf` which all other `.surf` sites use internally.
- There is 1 CDN under `file.base.surf`.
- There are at least 2 Google Cloud Run apps for more intensive things, related to `base.surf`.
- Then there are a bunch of vercel apps which render interfaces.
- The `base.surf` sites access a remote database.
- Initially for a while there will be no auth, just rate limiting.
- Eventually we can build an interface on top of base.surf to give access to the data.

## Example Paths

```
beat.surf/guitar/chord/c/major
beat.surf/guitar/scale/c/major
beat.surf/scale/c/major
beat.surf/piano/scale/c/major
beat.surf/piano/sample
beat.surf/sample
beat.surf/4
beat.surf/5
beat.surf/6
beat.surf/6/winters-dream
beat.surf/legal/privacy

task.surf/calculate/mortgage
task.surf/inspect/website/metadata
task.surf/inspect/font/name/a
task.surf/compare/font?a=x&b=y
task.surf/test/font/name&content=document
task.surf/sample/docx
task.surf/generate/password
task.surf/legal/privacy

seed.surf/users (random data)
seed.surf/pokemon
task.surf/api/v2/pokemon

tint.surf/hex
tint.surf/red
tint.surf/list/behr
tint.surf/palette

chat.surf/language/english/entry/hello
chat.surf/script/latin/a
chat.surf/language/english/noun
chat.surf/language/english/noun/2000
chat.surf/language/english/swadesh

text.surf/bible
text.surf/legal/privacy

code.surf/symbol

# symbols
code.surf/1
code.surf/u+1234

# gematria
code.surf/hello
code.surf/hello/gematria
# numerology
code.surf/john

# legal
code.surf/legal/privacy

# unicode block
code.surf/category/unicode
code.surf/category/unicode/latin
code.surf/category/arrows

call.base.surf
file.base.surf

form.surf
  Mathematical structures
  Generic truths
  Mapping Out Possibilities

  /math
  /myth
  /set
  /1000

calm.surf
  A website collecting visions, imaginations, and realizations about the structure of the universe and our purpose in it.
  /nothing
  /1000
    Connecting the dots.
  /3
    /poisons
  /vibe
  /universe
    /origin
  /vibe
  /3
    /vowels
  /4
  /code
    /alphabet
  /time
    /4:04
    /4:07
    /3:07
    /4:43
    /4:21
    /7:04
  /foragers
  /language
    /speech
      /origin
        /imagination
          /rock-chipping

view.surf
  /buddhism
    /tibetan
    /12
    Home page with grid of numbers.
  /hinduism
    /bhagavad-gita
  /christianity
  /test (flashcards)
  /judaism
    /sefirot
  /islam
    /literal
  /science
    /evolution
  /linguistics
  /observation
  /realization
```

code.surf has symbol information, as well as gematria/code/cypher/number information.

## Folder Structure

```
/moon
  /site
    /base.surf/base.surf
    /chat.surf/chat.surf
    /form.surf/form.surf
    /leaf.surf/leaf.surf
    /seed.surf/seed.surf
    /task.surf/task.surf
    /term.surf/term.surf
    /text.surf/text.surf
    /tone.surf/tone.surf
    /tune.surf/tune.surf
  /tool
    /vine.js
  /base
    /base-chat
    /base-file
    /base-mark
    /base-text
/star
  /tool
    /chat.js
    /chocolatey-task
    /flow.js
    /form.js
    /have.js
    /homebrew-load
    /kink-site.js
    /kink-text.js
    /kink.js
    /leaf
    /love-code.js
    /mesh.js
    /scan-link.js
    /site.js
    /size.js
    /talk.js
    /task
    /text.js
    /time.js
    /tint-text.js
    /tone-code.js
    /tone.js
    /work.js
```

## Sites

- `tone.surf`: Cross-language writing system.
- `tune.surf`: Intermediate spoken language.
- `term.surf`: Home base.
- `form.surf`: Structure definition books.
  - Patterns
  - Shapes
- `chat.surf`: Language site.
- `beat.surf`: Music site.
- `text.surf`: Texts.
- `code.surf`: Symbols.
  - Gematria calculator
  - Numbers
  - Names
- `tint.surf`: Colors.
- `base.surf`: Central hosting site.
  - base.surf/deck/pubmed/pubchem
- `task.surf`: Tools of all sorts.
  - HTML prettifier
  - Text to speech.
  - AI can possibly help make tools.
- `seed.surf`: Demo REST API data
- `note.surf`: Website demoing language.
  - A data format for humans.
  - base.note as the base file.
  - /form
    - Spec
  - /
    - Demo
  - /case/:case
    - Detailed examples
  - /flow
    - Notes on how to use it.
  - https://toml.io/en/
  - /zh/flow
- `star.surf`: Programming Language site.
  - sun logo
  - `star.surf/@foo/bar`: Hosting of packages.
- `leaf.surf`: Demo application.
  - file uploading
  - postgres integration
  - cloudflare integration
  - authentication
  - store files in ui
- `home.surf`
- `drum.surf`
- `leaf.surf`

## TODO

- define the schema of things
  - flow using ideas from work.js and base-chat
  - text
  - symbol
  - integer
  - integer-sequence
  - family-tree
- create the database schema
  - verify the database schema works locally with some samples of each data type.
- create the types for it
- use simple english language for defining schemas with machete
- define the api allowable fields calls (chat-surf.js)
- automatically serialize requests to and from postgres

Have ChatGPT/AI help me define and refine data models for various things.

- base.convert
- use base in all the projects

## How to Test

- base.surf locally connects to production database
- manually test queries against the production database
- insert data into the production database

Automated tests?

- local database
- clear database
- test inserting into database
- test querying database

## Data

- get word data, where is that again?
- get text data as json, where is that?
- put it into the base-chat and base-text repos.
- base-chat/import/wiktionary/en
- /export of saved files
- take the exports and import them into the production database

1. Wrangle the data into a standard form.
2. At the same time, refine the type definitions.
3. Export the data into a smaller set of files.
4. Load the exported files into the database.

The `base` TS library interacts with the REST API of `base.surf`.

Internally to `base.surf`, it calls the database functions and such.

base.parse(x)

The `base.surf` app uses `base` internally to parse the input, it just doesn't call `call` anywhere.

function update() {}

That lives in `base.surf` codebase.

Or there is a `base-work.js` internal library which does the database wrangling. No, just have it be in `base.surf`.

```
./actions
  /flow
    /update
```

We need to have a generic proxy api wrapper to centralize all the API calls.

base.surf
base.surf.call (proxy API, gcr)
base.surf.task (gcr)
base.surf.flow (gcr)

Maybe we have the flow functionality loaded into the base. Like machine learning models, it loads on startup. Then we just need one gcr.

- base.surf.call
  - can run all tasks
  - can perform flow functionality
  - can perform database calls

```
base.surf.call
  tool
    call
      flow make/save/read/toss
  seed (Load the data into the database)
  site (REST API handlers)
  form (types)
```

That goes to google cloud.

Have a `base` library which is used in the various projects which is a model system.

- hack.surf
- feel.surf
- star.surf
- crow.surf
- bolt.surf
- calm.surf
- fate.surf
- nest.surf
- bond.surf

The goal is to build a game?

/load/data/planets/:name
/load/data/v2/planets/:name

https://pokeapi.co/
