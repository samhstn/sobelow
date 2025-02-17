# Changelog

## v0.9.2
  * Bug Fixes
    * Fix error that resulted from redefining imported functions

## v0.9.1
  * Bug Fixes
    * Revert umbrella app recursion

## v0.9.0
  * Enhancements
    * Add `--mark-skip-all` and `--clear-skip` flags
    * New CSRF via action reuse checks
    * Sobelow can now be run in umbrella apps
     
  * Bug Fixes
    * Fix an error when printing some kinds of variables

## v0.8.0
  * Enhancements
    * Improve output consistency
        * All JSON findings contain `type`, `file`, and `line` keys
        * "Line" output now refers directly to the vulnerable line
        * Default output headers have been normalized
    
    **Note:** If you depend on the structure of the output, this 
    may be a breaking change. More information can be found at 
    [https://sobelow.io](https://sobelow.io).

## v0.7.8
  * Enhancements
    * Add `--threshold` flag
    * Add module names to finding output
    
  * Deprecations
    * File/Path check has been deprecated  
   
  * Bug Fixes
    * Fix inaccurate CSRF details

## v0.7.7
  * Enhancements
    * Add check for insecure websocket settings
    
  * Bug Fixes
    * Accept module attributes for application name

## v0.7.6

  * Bug Fixes
    * Fix issue that suppressed output options when config files were in use

## v0.7.5

  * Misc
    * Sobelow will now only halt when `--exit` flag is used

## v0.7.4

  * Bug Fixes
    * Log hardcoded secrets for txt output

## v0.7.3

  * Misc
    * Tweaks to `--out` flag.

## v0.7.2

  * Enhancements
    * Add router path to config findings
    * Add `--out` flag for writing to file

## v0.7.1

  * Enhancements
    * Improved handling of JSON format
    * Additional checks for File functions

## v0.7.0

  * Enhancements
    * Improved handling of vulnerabilities within templates.

  * Bug Fixes
    * Sobelow no longer incorrectly flags :binary `send_download` functions.

## v0.6.9

  * Enhancements
    * Improve template parsing and validation.
    * Support multiple routers, and improve route discovery.

  * Misc.
    * Update language for missing directory.

## v0.6.8

  * Bug Fixes
    * Fix bug in the handling of certain piped functions.
    * Revert not/in update that broke Elixir 1.4 compatibility.

## v0.6.7

  * Enhancements
    * Remove banner print from JSON format.

  * Bug Fixes
    * Fix error that occurred with certain function names in JSON format.

## v0.6.6

  * Enhancements
    * Add check for directory traversal via `send_download`
    * Add check for missing Content-Security-Policy
    * Check additional XSS vectors

## v0.6.5

  * Bug Fixes
    * Allow RCE module to be appropriately ignored.
    
## v0.6.4

  * Enhancements
    * Set timeout for version check.

## v0.6.3

  * Enhancements
    * Add RCE module to check for code execution via `Code` and `EEx`.
    
  * Deprecations
    * The `--with-code` flag has been changed to `--verbose`. The `--with-code` 
    flag will continue to work as expected until v1.0.0, but will print a 
    warning message.
