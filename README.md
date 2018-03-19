# Elixir Skills by Level

## Fundamentals

1. Data Types
	- Scalars
		- Integers
		- Floats
		- Strings (charlist vs binaries)
		- Atoms
		- Modules
		- Pids
			- Local
			- Remote
		- Functions
			- Anonymous Functions
			- Referencing Named Functions
	- Composite
		- Types
			- Tuples
			- Lists
			- Maps
			- Structs
			- [Erlang Proplists](http://erlang.org/doc/man/proplists.html)
			- [Elixir Keyword Lists](https://hexdocs.pm/elixir/Keyword.html)
		- Understand differences
			- Ordered vs Unordered
			- Cost of Updates
				- Prepend (for ordered types)
				- Append (for ordered types)
				- Arbitrary Insertion
				- Updating a Particular Element
			- Cost of Reads
				- Random Access
				- Sequential Access
2. Pattern Matching
	- Function Head
		- In Named Functions
		- In Anonymous Functions
	- Case Statement
	- Cond
	- With
	- Guards
	- Destructuring Data
		- Tuples
		- Lists
		- Maps
		- Structs
		- Especially Nested Structures
	- Pattern matching Operator (`=`) - Not Assignment!
3. Processes
	- [Create From Anonymous Function](https://hexdocs.pm/elixir/Kernel.html#spawn/1)
	- [Create from Named Function](https://hexdocs.pm/elixir/Kernel.html#spawn/3)
	- [Send Message to Process](https://hexdocs.pm/elixir/Kernel.html#send/2)
	- Receive Message From Another Process
	- Receive Message From Another Process With Timeout
	- [Exits](https://hexdocs.pm/elixir/Process.html#exit/2)
	- [Links](https://hexdocs.pm/elixir/Process.html#link/1)
	- Monitors
		- [Setting a Monitor](https://hexdocs.pm/elixir/Process.html#monitor/1)
		- [Removing a Monitor](https://hexdocs.pm/elixir/Process.html#demonitor/2)
	- Trapping Exits
4. Code Organization Techniques
	- `alias`
	- `import`
	- `require`
	- `use`

## Beginner (Using the STDLIB)
- [Using Observer](https://www.packtpub.com/mapt/book/application_development/9781784397517/1/ch01lvl1sec15/inspecting-your-system-with-observer)
- STDLIB & Data Structures
	- Essential
		- [Protocols](https://elixir-lang.org/getting-started/protocols.html)
		- [Enum](https://hexdocs.pm/elixir/Enum.html)
		- [Stream](https://hexdocs.pm/elixir/Stream.html)
		- [Elixir Sets](https://hexdocs.pm/elixir/MapSet.html)
	- Good to Have
		- [Erlang Sets](http://erlang.org/doc/man/sets.html)
		- [Erlang Queues](http://erlang.org/doc/man/queue.html)
		- [Erlang TreeSets](http://erlang.org/doc/man/gb_sets.html)
		- [Erlang Ordered Sets](http://erlang.org/doc/man/ordsets.html)
		- [Erlang Balanced Trees](http://erlang.org/doc/man/gb_trees.html)
		- [Erlang Directed Graphs](http://erlang.org/doc/man/digraph.html)
		- [Erlang Records](https://hexdocs.pm/elixir/Record.html)
- [Type & Function Specs](https://elixir-lang.org/getting-started/typespecs-and-behaviours.html#types-and-specs)
- [Behaviours](https://elixir-lang.org/getting-started/typespecs-and-behaviours.html#behaviours)
- [Timers](http://erlang.org/doc/man/timer.html)
	- Note the helper functions for converting to milliseconds

- [OTP Design Principles](http://erlang.org/doc/design_principles/des_princ.html)
	- [GenServer](https://hexdocs.pm/elixir/GenServer.html)
		- Client-side code vs "GenServer"-side code
		- Memorize all the Callbacks
		- [Structuring Your Module](https://medium.com/@CJPoll/opinion-genserver-best-practices-for-elixir-f53d3b060dbf)
		- Registering the GenServer:
			- Locally
			- In an Elixir `Registry`
			- Globally across a cluster
	- [Supervisor](https://hexdocs.pm/elixir/Supervisor.html#content)
		- [Supervision Strategies](https://hexdocs.pm/elixir/Supervisor.html#module-strategies)
			- :one_for_one
			- :one_for_all
			- :rest_for_one
			- :simple_one_for_one
			- DynamicSupervisor
		- [Shutdown Values](https://hexdocs.pm/elixir/Supervisor.html#module-shutdown-values-shutdown)
			- :brutal_kill
			- :infinity
			- timeout
		- [Restart Values](https://hexdocs.pm/elixir/Supervisor.html#module-restart-values-restart)
			- :permanent
			- :temporary
			- :transient
		- [Child Specs](https://medium.com/@CJPoll/opinion-genserver-best-practices-for-elixir-f53d3b060dbf)
	- [Application](https://hexdocs.pm/elixir/Application.html#content)
	- [Task](https://hexdocs.pm/elixir/Task.html#content)
	- [Agent](https://hexdocs.pm/elixir/Agent.html#content)
	- [Generic State Machines](http://erlang.org/doc/design_principles/statem.html)
	- [Ecto](https://hexdocs.pm/ecto/Ecto.html)
	- [Plug](https://github.com/elixir-plug/plug)
	- [Phoenix](https://hexdocs.pm/phoenix/overview.html)

## Intermediate

- [ETS](http://erlang.org/doc/man/ets.html)
- [DETS](http://erlang.org/doc/man/dets.html)
- [Efficiency Guide User's Guide](http://erlang.org/doc/efficiency_guide/users_guide.html)
- [Built-In OS Monitoring Utilities](http://erlang.org/doc/search/)
- Process Pooling
	- [Process Groups](http://erlang.org/doc/man/pg2.html)
	- [Poolboy](https://github.com/devinus/poolboy)
- [RPC](http://erlang.org/doc/man/rpc.html)

## Advanced

- Macros & Metaprogramming