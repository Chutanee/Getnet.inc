# Getnet: Activity command

usage: am [subcommand] [options]

usage: am start [-D] [-N] [-W] [-P <FILE>] [--start-profiler <FILE>]

               [--sampling INTERVAL] [-R COUNT] [-S]

               [--track-allocation] [--user <USER_ID> | current] <INTENT>

       am startservice [--user <USER_ID> | current] <INTENT>

       am stopservice [--user <USER_ID> | current] <INTENT>

       am broadcast [--user <USER_ID> | all | current] <INTENT>

       am to-uri [INTENT]

       am to-intent-uri [INTENT]

       am to-app-uri [INTENT]

am start: start an Activity.  Options are:

    -D: enable debugging

    -N: enable native debugging

    -W: wait for launch to complete

    --start-profiler <FILE>: start profiler and send results to <FILE>

    --sampling INTERVAL: use sample profiling with INTERVAL microseconds

        between samples (use with --start-profiler)

    -P <FILE>: like above, but profiling stops when app goes idle

    -R: repeat the activity launch <COUNT> times.  Prior to each repeat,

        the top activity will be finished.

    -S: force stop the target app before starting the activity

    --track-allocation: enable tracking of object allocations

    --user <USER_ID> | current: Specify which user to run as; if not

        specified then run as the current user.

    --stack <STACK_ID>: Specify into which stack should the activity be put.

am startservice: start a Service.  Options are:

    --user <USER_ID> | current: Specify which user to run as; if not

        specified then run as the current user.

am stopservice: stop a Service.  Options are:

    --user <USER_ID> | current: Specify which user to run as; if not

        specified then run as the current user.

am broadcast: send a broadcast Intent.  Options are:

    --user <USER_ID> | all | current: Specify which user to send to; if not

        specified then send to all users.

    --receiver-permission <PERMISSION>: Require receiver to hold permission.

am to-uri: print the given Intent specification as a URI.

am to-intent-uri: print the given Intent specification as an intent: URI.

am to-app-uri: print the given Intent specification as an android-app: URI.

<INTENT> specifications include these flags and arguments:

    [-a <ACTION>] [-d <DATA_URI>] [-t <MIME_TYPE>]

    [-c <CATEGORY> [-c <CATEGORY>] ...]

    [-e|--es <EXTRA_KEY> <EXTRA_STRING_VALUE> ...]

    [--esn <EXTRA_KEY> ...]

    [--ez <EXTRA_KEY> <EXTRA_BOOLEAN_VALUE> ...]

    [--ei <EXTRA_KEY> <EXTRA_INT_VALUE> ...]

    [--el <EXTRA_KEY> <EXTRA_LONG_VALUE> ...]

    [--ef <EXTRA_KEY> <EXTRA_FLOAT_VALUE> ...]

    [--eu <EXTRA_KEY> <EXTRA_URI_VALUE> ...]

    [--ecn <EXTRA_KEY> <EXTRA_COMPONENT_NAME_VALUE>]

    [--eia <EXTRA_KEY> <EXTRA_INT_VALUE>[,<EXTRA_INT_VALUE...]]

        (mutiple extras passed as Integer[])

    [--eial <EXTRA_KEY> <EXTRA_INT_VALUE>[,<EXTRA_INT_VALUE...]]

        (mutiple extras passed as List<Integer>)

    [--ela <EXTRA_KEY> <EXTRA_LONG_VALUE>[,<EXTRA_LONG_VALUE...]]

        (mutiple extras passed as Long[])

    [--elal <EXTRA_KEY> <EXTRA_LONG_VALUE>[,<EXTRA_LONG_VALUE...]]

        (mutiple extras passed as List<Long>)

    [--efa <EXTRA_KEY> <EXTRA_FLOAT_VALUE>[,<EXTRA_FLOAT_VALUE...]]

        (mutiple extras passed as Float[])

    [--efal <EXTRA_KEY> <EXTRA_FLOAT_VALUE>[,<EXTRA_FLOAT_VALUE...]]

        (mutiple extras passed as List<Float>)

    [--esa <EXTRA_KEY> <EXTRA_STRING_VALUE>[,<EXTRA_STRING_VALUE...]]

        (mutiple extras passed as String[]; to embed a comma into a string,

         escape it using "\,")

    [--esal <EXTRA_KEY> <EXTRA_STRING_VALUE>[,<EXTRA_STRING_VALUE...]]

        (mutiple extras passed as List<String>; to embed a comma into a string,

         escape it using "\,")

    [-f <FLAG>]

    [--grant-read-uri-permission] [--grant-write-uri-permission]

    [--grant-persistable-uri-permission] [--grant-prefix-uri-permission]

    [--debug-log-resolution] [--exclude-stopped-packages]

    [--include-stopped-packages]

    [--activity-brought-to-front] [--activity-clear-top]

    [--activity-clear-when-task-reset] [--activity-exclude-from-recents]

    [--activity-launched-from-history] [--activity-multiple-task]

    [--activity-no-animation] [--activity-no-history]

    [--activity-no-user-action] [--activity-previous-is-top]

    [--activity-reorder-to-front] [--activity-reset-task-if-needed]

    [--activity-single-top] [--activity-clear-task]

    [--activity-task-on-home]

    [--receiver-registered-only] [--receiver-replace-pending]

    [--receiver-foreground] [--receiver-no-abort]

    [--receiver-include-background]

    [--selector]

    [<URI> | <PACKAGE> | <COMPONENT>]

$

$
