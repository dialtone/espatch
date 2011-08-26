This is shameless copy of Basho's WebMachine dispatch library.

There is virtually no difference except for:

      https://github.com/basho/webmachine/blob/2be260f0e1c41a861022d0c5a9996fcd66edf8a3/src/webmachine_dispatcher.erl#L203

This line merges data obtained during dispatching back in the webmachine Request object.

By removing that line I force everyone to do this operation, if they need to, in a Guard that will receive the information during matching and an object passed in by the caller.

There is really nothing else new here for now.