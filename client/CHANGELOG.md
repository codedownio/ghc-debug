# Revision history for ghc-debug-client

## 0.7.0.0 -- 2025-05-20

* Relax version bounds

## 0.6.0.0 -- 2024-04-10

* Properly handle exceptions in parralel traversals
* Fix snapshotting when extra blocks are requested by RequestBlock
* Support for profiling RTS

## 0.5.0.0 -- 2023-06-06

* Remove eventlog2html dependency and hence `profile` function. These can be
  implemented in your own library if you want to use them.
* Update with support for ghc-9.4 and ghc-9.6.
* Add support for debugging over a TCP socket (`withDebuggeeConnectTCP`)


## 0.4.0.1 -- 2023-03-09

* Relax some version bounds and use eventlog2html 0.9.3

## 0.4 -- 2022-12-14

* Add support for tracing SRTs. This is quite an invasive change which adds a new
  pointer type to the DebugClosure type. This change is reflected in the API for
  parTrace and traceFrom.

* The `Quadtraverse` abstraction is generalised to `Quintraverse` to account for
  this new type parameter.

## 0.3 -- 2022-10-06

* Abstract away tracing functions to allow configuration of progress reporting.
* Add stringAnalysis and arrWordsAnalysis in GHC.Debug.Strings
* Make block decoding more robust if the cache lookup fails for some reason.
* Fix bug in snapshots where we weren't storing stack frame source locations or
  version.

## 0.2.1.0 -- 2022-05-06

* Fix findRetainersOfConstructorExact

## 0.2.0.0 -- 2021-12-06

* Second version.

## 0.1.0.0 -- 2021-06-14

* First version.
