# Elixir Skills by Level

[A Bunch of Books on Elixir](https://github.com/h4cc/awesome-elixir#books)

## Fundamentals

1. Data Types
	- Scalars
		- [Integers](https://elixir-lang.org/getting-started/basic-types.html#basic-arithmetic)
		- [Floats](https://elixir-lang.org/getting-started/basic-types.html#basic-arithmetic)
		- Strings (charlist vs binaries)
		- [Atoms](https://elixir-lang.org/getting-started/basic-types.html#atoms)
		- [Booleans](https://elixir-lang.org/getting-started/basic-types.html#booleans)
		- [Modules & Functions](https://elixir-lang.org/getting-started/modules-and-functions.html)
		- [Pids](https://elixir-lang.org/getting-started/processes.html)
			- Local
			- Remote
		- Functions
			- [Anonymous Functions](https://elixirschool.com/en/lessons/basics/functions/#anonymous-functions)
			- [Referencing Named Functions](https://elixir-lang.org/getting-started/modules-and-functions.html#function-capturing)
	- Composite
		- Types
			- [Tuples](https://elixir-lang.org/getting-started/basic-types.html#tuples)
			- [Lists](https://elixir-lang.org/getting-started/basic-types.html#linked-lists)
			- [Keyword Lists](https://elixir-lang.org/getting-started/keywords-and-maps.html#keyword-lists)
			- [Maps](https://elixir-lang.org/getting-started/keywords-and-maps.html#maps)
			- [Structs](https://elixir-lang.org/getting-started/structs.html)
			- [Erlang Proplists](http://erlang.org/doc/man/proplists.html)
			- [Elixir Keyword Lists](https://hexdocs.pm/elixir/Keyword.html)
		- Understand differences between these types
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
	- [Match Operator](https://elixir-lang.org/getting-started/pattern-matching.html#the-match-operator) (`=` - Not Assignment!)
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
3. Processes
	- [Create From Anonymous Function](https://hexdocs.pm/elixir/Kernel.html#spawn/1)
	- [Create from Named Function](https://hexdocs.pm/elixir/Kernel.html#spawn/3)
	- [Send Message to Process](https://hexdocs.pm/elixir/Kernel.html#send/2)
	- [Receive Message From Another Process](https://elixir-lang.org/getting-started/processes.html#send-and-receive)
	- [Receive Message From Another Process With Timeout](https://elixir-lang.org/getting-started/processes.html#send-and-receive)
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

## Beginner (Learning The Ecosystem)

- [Type & Function Specs](https://elixir-lang.org/getting-started/typespecs-and-behaviours.html#types-and-specs)
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
- [Behaviours](https://elixir-lang.org/getting-started/typespecs-and-behaviours.html#behaviours)
- [Timers](http://erlang.org/doc/man/timer.html)
	- Note the helper functions for converting to milliseconds
- [ExDoc](https://github.com/elixir-lang/ex_doc)
	- Generate documentation for your own projects
- [gen_tcp](http://erlang.org/doc/man/gen_tcp.html)
	- Facilities for interacting with raw TCP sockets (both server and client side)
- [gen_udp](http://erlang.org/doc/man/gen_udp.html)
	- Like gen_tcp, but for UDP
- [OTP Design Principles](http://erlang.org/doc/design_principles/des_princ.html)
	- [GenServer](https://hexdocs.pm/elixir/GenServer.html)
		- Client-side code vs "GenServer"-side code
		- Memorize all the Callbacks
		- [Structuring Your Module](https://medium.com/@CJPoll/opinion-genserver-best-practices-for-elixir-f53d3b060dbf)
		- [Registering the GenServer](https://hexdocs.pm/elixir/GenServer.html#module-name-registration)
			- Locally
			- In an Elixir [Registry](https://hexdocs.pm/elixir/Registry.html#content)
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
		- [Child Specs](https://hexdocs.pm/elixir/Supervisor.html#module-child-specification)
	- [Application](https://hexdocs.pm/elixir/Application.html#content)
	- [Task](https://hexdocs.pm/elixir/Task.html#content)
	- [Agent](https://hexdocs.pm/elixir/Agent.html#content)
	- [Generic State Machines](http://erlang.org/doc/design_principles/statem.html)
- [Logger](https://hexdocs.pm/logger/Logger.html)
- Ecosystem
	- [Ecto](https://hexdocs.pm/ecto/Ecto.html)
		- Data Validation Library
		- Also useful as an ORM
	- [Plug](https://github.com/elixir-plug/plug)
	- [Phoenix](https://hexdocs.pm/phoenix/overview.html)
	- [HTTPoison](https://github.com/edgurgel/httpoison)
	- JSON Libs
		- [Poison](https://github.com/devinus/poison) - Pure Elixir
		- [Jason](https://github.com/michalmuskala/jason) - Pure Elixir
		- [Jiffy](https://github.com/davisp/jiffy) - Drops to C (fastest in the west)

## Intermediate (More Advanced Use of STDLIBs and Ecosystem)

- [Dialyzer](http://erlang.org/doc/apps/dialyzer/dialyzer_chapter.html)
- [Dialyxir](https://github.com/jeremyjh/dialyxir) - A wrapper for including Dialyzer in mix projects
- [ETS](http://erlang.org/doc/man/ets.html) - In-memory data store for arbitrary erlang/elixir data structures
- [DETS](http://erlang.org/doc/man/dets.html) - Disk-based data store for arbitrary erlang/elixir data structures
- [Efficiency Guide User's Guide](http://erlang.org/doc/efficiency_guide/users_guide.html)
- [Built-In OS Monitoring Utilities](http://erlang.org/doc/search/)
- Process Pooling
	- [Process Groups](http://erlang.org/doc/man/pg2.html)
	- [Poolboy](https://github.com/devinus/poolboy)
- [RPC](http://erlang.org/doc/man/rpc.html)
- [GenStage](https://hexdocs.pm/gen_stage/GenStage.html)
- [Flow](https://hexdocs.pm/flow/Flow.html)

## Advanced

- [Erlang in Anger](http://www.erlang-in-anger.com/)
	- Great ebook on dealing with misbehaving Erlang/Elixir stuff
- Clustering
- [Mnesia](http://erlang.org/doc/man/mnesia.html)
	- A database built on ETS and DETS with transactions and other good features.
	- Definitely not an RDBMS. Learn the tradeoffs it makes before using (as with any database)
- Macros & Metaprogramming
