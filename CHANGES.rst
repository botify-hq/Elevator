
0.4 / 2012-10-22
==================

  * Add: restore theme
  * Add : Base sphinx documentation
  * Update : new License MIT
  * Fix #86: IOError when bad config file supplied as cmdline argument
  * Fix #95: Elevator will start and log errors even though some databases are corrupted
  * Fix : log-level debug messages format
  * Fix : travis, tests, requirements

0.3d / 2012-10-19
==================

  * Add : Request error for invalid request messages
  * Update #91: Mount default at server startup
  * Update #91: Mount/Unmount command + auto-mount on connect
  * Update #91: add a ticker class, which executes a function every x seconds
  * Update #30, Update #99: Compress Responses on demande (request.meta['compression'])
  * Update #88, Update #99: now responses comes in two parts header+content
  * Update #88: Fix MGet, Range, Slice return values types to suite with new responses format
  * Update #88: Refactored Request/Responses format
  * Update : Refactored DatabasesHandler internal storage
  * Update : Few refactoring on loggers handling
  * Update : Refactored DBConnect no more db_uid to provide in request
  * Fix #97: provide mono-letters args
  * Fix #89: Log requests/responses on log-level=DEBUG
  * Fix #87: Refactored logging
  * Fix #100: Non blocking workers, graceful shutdown == PERFORMANCES
  * Fix #98: Activity logging on both file and stdout
  * Fix #101: fixed ipc handling
  * Fix : api tests for compatibility with new Req/Resp
  * Fix : refactored tests for new Range/Slice behavior when size == 1
  * Fix : Mount/Unmount passed args

