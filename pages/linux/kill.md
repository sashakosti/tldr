# kill

> Sends a signal to a process, usually related to stopping the process.
> All signals except for SIGKILL and SIGSTOP can be intercepted by the process to perform a clean exit.
> More information: <https://manned.org/kill>.

- Terminate a program using the default SIGTERM (terminate) signal:

`kill {{process_id}}`

- List signal values and their corresponding names (to be used without the `SIG` prefix). The available options may depend on the `kill` implementation:

`kill {{-l|-L|--table}}`

- Terminate a background job:

`kill %{{job_id}}`

- Terminate a program using the SIGHUP (hang up) signal. Many daemons will reload instead of terminating:

`kill -{{1|HUP}} {{process_id}}`

- Terminate a program using the SIGINT (interrupt) signal. This is typically initiated by the user pressing `<Ctrl c>`:

`kill -{{2|INT}} {{process_id}}`

- Signal the operating system to immediately terminate a program (which gets no chance to capture the signal):

`kill -{{9|KILL}} {{process_id}}`

- Signal the operating system to pause a program until a SIGCONT ("continue") signal is received:

`kill -{{17|STOP}} {{process_id}}`

- Send a `SIGUSR1` signal to all processes with the given GID (group id):

`kill -{{SIGUSR1}} -{{group_id}}`
