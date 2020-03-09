# notes-polyconf-2016

:book: Notes from conference: PolyConf 2016 — https://16.polyconf.com/

> Wydarzenia trwało od 2016-06-30 do 2016-07-02.

## Day I

### 1. "Introduction"

Organizator przedstawił jakie problematyczne i stresujące jest organizowanie
takiego wydarzenia jakim jest konferencja. Podzielił się z nami informacją,
że stan konta bankowego na dzień _1 czerwca_ to `-18k euro`.

Z różnych źródeł wiem, że Zaiste reklamował projekt: http://eventil.com,
ale nie użył nazwy tego projektu. Zastanawiające: Dlaczego nie podał adresu?
Nie miał czym się pochwalić? Nie chciał być nachalny?

### 2. "Introducing clojure.spec" Arne Brasseur

* :movie_camera: Talk — https://www.youtube.com/watch?v=CVO0M8CTV78
* :page_with_curl: Slajdy — http://arnebrasseur.net/talks/2016-clojure-spec/

### 3. "Functional Thinking" Artur Czajka

* :movie_camera: Talk — https://www.youtube.com/watch?v=Nx9pEQng8H8

### 4. "Elm for JavaScript Developers" Jack Franklin

* :movie_camera: Talk — https://www.youtube.com/watch?v=tOkOmWgDLOM
* :page_with_curl: Slajdy — https://speakerdeck.com/jackfranklin/polyconf-elm-for-js-developers

<details>

Dodatki - https://github.com/jackfranklin/elm-for-js-developers-talk/tree/polyconf

Prelegent polecał przeczytać: http://staltz.com/unidirectional-user-interface-architectures.html

Najważniejszą zasadą w Elm-ie jest "brak błędów podczas życia aplikacji".
czyli: "No runtime errors"

Zasady:

* expressive, clear code
* clean syntax
* self-documented: types
* robust
* immutability = not mutate objects
* modules systems
* everything is scopes

We don't have `undefined`, `null` but `Maybe` (Nothing)

Commands and (Signals =>) Subscriptions

#### The Elm Architecture

* model
* view
* update

</details>

### 5. "Lwan project: an experimental, scalable, high-performance HTTP server" Leandro Pereira

* :movie_camera: Talk — https://www.youtube.com/watch?v=cttY9FdCzUE

### 6. "Dynamics of change: why reactivity matters" Andre Staltz

* :movie_camera: Talk — https://www.youtube.com/watch?v=v68ppDlvHqs
* :page_with_curl: Slajdy — https://speakerdeck.com/staltz/dynamics-of-change-why-reactivity-matters
* :postbox: Kontakt — https://github.com/staltz
* :postbox: Kontakt — https://twitter.com/andrestaltz

<details>

Jak dla mnie była to najlepsza prelekcja.

#### Spoiler

Po wysłuchaniu wszystkich prelekcji dostępnych podczas konferencji,
jestem w stanie powiedzieć, że była to najlepsza prelekcja dla mnie z kilku powodów:

* świetnie przygotowanie prowadzącego
* bardzo dobrze zrobione slajdy
* nauczyłem się z tego prelekcji dużo nowych rzeczy
* jako jedna z nielicznych prelekcji pchnęła mnie do przodu w moim rozwoju osobistym
* dzięki tej prelekcji będę chciał opisać na blogu pewien wzorzec projektowy,
    który był podczas prelekcji omawiany

</details>

### 7. "Becoming a Polyglot - APIs in 4 Languages" Kirsten Hunter

* :movie_camera: Talk — https://www.youtube.com/watch?v=ZfqfLpV26yY

### 8. "Dynamic Linking in the Browser" Guy Bedford

* :movie_camera: Talk — https://www.youtube.com/watch?v=cRSBi1EAOCo

<details>

* Loader specification - https://whatwg.github.io/loader/
* Pusher - https://pusher.com/docs/javascript_quick_start

    ```html
    <script type="module">
        import {fn} from './lib/js';
        fn();
    </script>

    <script type="module" src="./lib.js"></script>
    ```

* dynamic browser module resolution
* http/2 push
* dynamic resolution today?

"SystemJS is a polyfill for full specification" tak powiedział prelegent.

</details>

### LIGHTNING TALKS :zap:

* :movie_camera: Talks — https://www.youtube.com/watch?v=de-EiEXo3tA

---
---
---

## Day 2

### 1. "Oden - A Functional Programming Language for the Go Ecosystem" Oskar Wickström

* :movie_camera: Talk — https://www.youtube.com/watch?v=qRm_58RA9ns

### 2. "Pick Your Battles" Zef Hemel

* :movie_camera: Talk — https://www.youtube.com/watch?v=J_44tCwpChY
* :page_with_curl: Slajdy — https://speakerdeck.com/zef/pick-your-battles
* :postbox: Kontakt — http://zef.me
* :postbox: Kontakt — http://twitter.com/zef

<details>

Prelekcja w oparciu o artykuł - http://zef.me/blog/4235/pick-your-battles

Wnioski:

* nie próbuj używać nowych rzeczy, gdy zaczynasz startup tylko dlatego, że są nowe
* bądź pragmatyczny, używaj języków, narzędzi zgodnie z ich przeznaczeniem

</details>

### 3. "Back to Basics: Discussing Prototypes with the Terminator" Christoph Gockel

* :movie_camera: Talk — https://www.youtube.com/watch?v=6rVfqhtWJ6g

### 4. "Scaling React Applications" Max Stoiber

* :movie_camera: Talk — https://www.youtube.com/watch?v=iNNiqWZtUHg
* :postbox: Kontakt — https://twitter.com/mxstbr

<details>

* What is scalability?
* System can handle more users, requests than application?

#### State management

##### flux - unidirectional data flow

* problem, because based on events
* hard to test

##### redux

* in functional style
* better fo tests, add middleware

#### Architecture

* containers contains components
* components access to state
* group files by feature
* use redux-saga

#### Performance

#### Webpack: Code Splitting

#### ImmutableJS

* porównywanie dużych obiektów bardzo szybko, bo porównywane sa tylko hashe tych obiektów
* create new data-structure: record

</details>

### 5. "Getting your Node.js app production ready" Zbyszek Tenerowicz

* :movie_camera: Talk — https://www.youtube.com/watch?v=hME4c8y_B-s
* :movie_camera: Talk — https://www.youtube.com/watch?v=orLYv91T5io
* :page_with_curl: Slajdy — http://naugtur.pl/pres3/node2prod/
* :postbox: Kontakt — http://twitter.com/naugtur

<details>

#### pm2

* http://pm2.keymetricts.io

#### basic monitoring

* server resources
* is app running
* can app be accessed

old monitoring with people is better than any fany tool for that

#### but first: some good practices

* app should be stateless
* redis ONLY for storing temporary data

#### Asynchronous all the things!

* promises
* did you know async JSON parsers exists? yes, exists
* `npm shrinkwarap` - helpful tool before go to production
* Node Security Project and requireSafe

Logging: if you expect more tha one user, generate a random ID for
each HTTP request and add it to all logs it generates

fatal, error are pretty obcios

warn can be an error you don't mind

info is for tracing what app does regularly

debug is for logs that help you understand what up

trace should contains enough data to reproduce

Enabling changing log level without restart the app, most bugs top

#### sanitize your logs

* logs should not contains user credentials etc
* build a sanitizer

#### what to monitor

* watch for 5xx and alert immediately

#### loop blocks

* use 'blocked' to detect

```javascript
blocked(function (ms) {
    console.log(ms);
});
```

#### memory increase

* Node.js will whatsdown 1.5GB gets allocated
* monitor process.memoryUsage.rss
* watch for steady increase in memory use

#### debugging memory leaks

* v8-profiles in dev/staging
* simple tutorial (https://github.com/felixge/node-memory-leak-tutorial) from 5yr ago, but still works
* in production - tak a heapdump and then another, compare

#### more

* getting and using heap dumps
* error handler shared across the app
* feature toggles
* much more security tips
* safe, non leaking, object caches
* no-downtime redeploys

</details>

### 6. "OOP -> FP" Julia Gao

* :movie_camera: Talk — https://www.youtube.com/watch?v=R_TQtthAGQc
* :page_with_curl: Slajdy — http://slides.com/ryoia/oop-to-fp

### 7. "Owning Ownership: How Thinking About Ownership Prevents Bugs" Sean Griffin

* :movie_camera: Talk — https://www.youtube.com/watch?v=PBV6j2BhEGE
* :postbox: Kontakt — http://twitter.com/sgrif
* :postbox: Kontakt — http://github.com/sgrif

<details>

* Lib: Diesel - http://diesel.rs
* Podcast - http://bikeshed.fm

</details>

---

### LIGHTNING TALKS :zap:

* :movie_camera: Talks — https://www.youtube.com/watch?v=AbqByKfar8o

---

### 8. "The Linguistic Relativity of Programming Languages" Jenna Zeigen

* :movie_camera: Talk — https://www.youtube.com/watch?v=XV3vUZ9y8AU

### 9. "Nim async voodoo" Andreas Rumpf

* :movie_camera: Talk — https://www.youtube.com/watch?v=hwArqelfBBY
* :page_with_curl: Slajdy — https://github.com/araq/polyconf2016

<details>

#### NIM = New programming language!

* compiled to js
* statically typed
* python inspired syntax

</details>

### 10. "Why System Programming is for Everyone" Julia Evans

* :movie_camera: Talk — https://www.youtube.com/watch?v=HjASqh5z8ck

<details>

Prelegentka pokazała mnóstwo interesujących programów:

* `strace` - favorite tool of Julia
* `opensnoop` - http://github.com/iovisor/bcc
* `wireshark` — frame contains "GET"
* `ngrep`
* `dstat` - print whats happened on system
* `perf` - next favorite tool

</details>

### 11. "The Seif Project" Douglas Crockford

* :movie_camera: Talk — https://www.youtube.com/watch?v=O9AwYiwIvXE

<details>

Prelegent opowiadał o projekcie Seif, który to ma być lekiem
na obecne problemy z hasłami i generalnie z kradzieżą dostępu
do dowolnych danych.

Projekt **Seif** będzie opierał się na dostępach do klucza osoby,
która chce skorzystać z danego zasobu.

* Link do projektu na GitHubie - https://github.com/paypal/seifnode
* Wprowadzenie do projektu z innej konferencji - https://www.oreilly.com/learning/introducing-the-seif-project

</details>

---
---
---

## Day 3

### 1. "Erlang in The Land of Lisp" Jan Stępień

* :movie_camera: Talk — https://www.youtube.com/watch?v=qVMKIKJrUd8
* :postbox: Kontakt — http://twitter.com/janstepien

<details>

#### The Erlang VM

where processes dwell

* concurrency - as many shed as meny cpu you have

#### Rib - Request in batches.

* Repozytorium - https://github.com/stylefruits/rib

#### rebar - Package manager of erlang

</details>

### 2. "Exploring The Universal Library" Szymon Kaliski

* :movie_camera: Talk — https://www.youtube.com/watch?v=qByrsLPxjHs

<details>

* http://thi.org - set of libs for closure and closure script
* http://pex.gl
* http://yt.com/watch?q=Sbd4NX95Ysc

</details>

### 3. "Language-agnostic static analysis with abstract ASTs" Marcin Wyszyński

* :movie_camera: Talk — https://www.youtube.com/watch?v=0YHXFY_NSfA

<details>

* http://twitter.com/codebeatapp
* antlr - fantastic ast analyzer

</details>

### 4. "My adventure with Elm" Yan Cui

* :movie_camera: Talk — https://www.youtube.com/watch?v=28jCDXfZCgE
* :postbox: Kontakt — http://twitter.com/theburningmonk

<details>

* https://github.com/theburningmonk/elm-snake
* http://elm-lang.org/try
* http://www.slideshare.net/theburningmonk/my-adventure-with-elm-polyconf-16

</details>

### 5. "Ecto vs. ActiveRecord: A Tale of Two ORMs" Brad Urani

* :movie_camera: Talk — https://www.youtube.com/watch?v=96YwY7Lld0Q
* :postbox: Kontakt — http://twitter.com/bradurani

<details>

Ecta.Repo, Schema, Changesets, Query

</details>

### 6. "Datomic in production, 1 year in" Hans Hübner

* :movie_camera: Talk — https://www.youtube.com/watch?v=0y6QK813new
* :postbox: Kontakt — https://twitter.com/hanshuebner

<details>

#### datomic - power database

* written by native closure
* immutable
* unique of datomic architecture is transactions
* file transfer monitor
* data model matcher
* biggest issue - long transactions
* garbage collection is a problem
* migration are a huge problem with datomic

</details>

### 7. "Kemal: Building Lightning Fast Web Applications with Simplicity" Serdar Dogruyol

* :movie_camera: Talk — https://www.youtube.com/watch?v=KJB-nAoRSr8
* :postbox: Kontakt — http://twitter.com/sdogruyol

<details>

#### Crystal - new programming lang: https://crystal-lang.org/

* ruby like (not compatible)
* compiled
* type inference
* concurrency via channels (a la Go)
* metaprogramming via Macros
* Native Code via LLM

#### Kemal

* HTTP verbs - RESTful
* Built-in WebSocket
* http://kemal-react-chat.herokuapp.com/
* Streamable Request / Response Context
* Built-in
* Middlewares

</details>

---

### LIGHTNING TALKS :zap:

<details>

#### music

* overtone - https://github.com/overtone/overtone
* shadertone - https://github.com/overtone/shadertone
* clousure

#### git

```bash
git diff --compaction-heuristic ## set as default
git push --force-with-lease
```

#### keyboard

* http://stevelosh.com/blog/2012/10/a-modern-space-cadet/

</details>

---

### 8. "Experience report: Clojure on iOS with React Native" Jelle Akkerman

* :movie_camera: Talk — https://www.youtube.com/watch?v=UHRITqJGadU
* :postbox: Kontakt — http://twitter.com/jellea
* :postbox: Kontakt — http://github.com/jellea

<details>

#### ClojureScript

* closure to js
* source maps
* rock solid js two way interoperability
* google closure under the ood for max perf
* useful (immutable) data structures
* logic programming
* pattern matching
* csp
* bootstrapped compiler

#### Landscape

* natal - ambly (webdev)
* re-natal (lein figwheel websocket)
* boot-react-native (boot-reload websocket)
* ktoa  (re-natal + webapp)
* cljsrn-desktop  (ambly + os x app)

#### Positives

* fasts! no more slow web views
* easy cuz rect
* 3 ecosystems

#### Sky/CPU is the limit!

* pick your weapon: om next, reagent

#### Hiccup example

#### Debugging

* tools in xcode simulator
* chrome debugger
* source maps
* ClojureScript repl

#### Testing

* unit test i ncljs
* integration in kif

#### Hurdles

* styling without ss is hard
* navigator is super imperative
* react native moves fast and upgrades are a pain
* tooling was very brittle
* oh provision profiles

#### Problem 1: Styling

* show example - bad composability
* bas reusability
* responsiveness
* 4 vs 12k different screen sizes
* I want BASS css utility based css!

#### Introducing Lookbook

* open source CLJS lib for composable styling targeted at React Native
* precompiles - performance

#### Problem 2: Tooling

* only whitespace CLJS compilation possible
* hot reload
* source maps
* solved by boot-react-native and re-natal
* never touch xcode again - win!
* upgrading is still a mess

#### TODO

* give re-natal or boot-stract-native a sping
* try it with lookbook
* subscribe to my UI newsletter
* buy a present for yourself or a friend with the Fly app

http://iamfy.co

</details>

### 9. "From Unikernels to Databases to UIs: Truly full-stack apps in OCaml" Sean Grove

* :movie_camera: Talk — https://www.youtube.com/watch?v=F2dPXk__B6M
* :postbox: Kontakt — http://twitter.com/sgrove
* :postbox: Kontakt — http://github.com/sgrove

<details>

... as Hype-man

#### App Dev Goals

* security
* correctness (fewer bugs, please)
* performance
* code reuse
* maintainability
* delivery speed

#### OCaml

* incredibility  lightweight but thorough type system
* figure out type of statement
* statically compiled with predictable characteristics
* compile to highly efficient js - use with React
* compile to arm
* encourages function style

#### unikernels

* new way of building and deploying apps
* operating system as a library
* pure OCaml - implementation of low-level libraries: TCP/IP, TLS, Data storage
* compiled ahead of time
* your app is entire VM

#### OCaml Caveats

* tooling, namespacing, etc. are nightmares
* learning resources can be outdated
* syntax can off-putting
* community is significantly smaller than many others
* errors can be inscrutable
* single-core

#### Reason

* FB has invested hugely into OCaml tooling with Reason
* meta-lang on top of OCaml

</details>

### 10. "A brief history of the ML family" Rachel Reese

* :movie_camera: Talk — https://www.youtube.com/watch?v=cbDjpi727aY

<details>

* OCalm created in 1996
* F## is first open source MS language in 2010
* http://fsharp.org
* in 2016: nearly 1000 members, training
* F## move to github 2015

</details>

### 11. "Knit, Chisel, Hack: Building Programs in Guile Scheme" Andy Wingo

* :movie_camera: Talk — https://www.youtube.com/watch?v=TVO8WXFYDIA
* :postbox: Kontakt — https://twitter.com/andywingo

<details>

* https://wingolog.org/
* https://gnu.org/s/guix
* https://gnu.org/s/guile

</details>
