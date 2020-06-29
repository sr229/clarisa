# Project Duet (aka Clarisa)

Project Duet is a new architecture based on learnings from [Clara](https://github.com). The idea on the bot architecture we wanted to go was:

- The developer shouldn't worry about memory management, or managing things like presence updates, events, and so on.
- The gateway should be flexible - it doesn't need to be overly complicated to be used. APIs it represent should allow the developer to be more productive.
- You only implement commands, the rest is on us.

Hence, what came up was known as "Project Duet" - a bot gateway for Discord designed to do exactly that. Using gRPC, Project Duet bots only need to implement the things that matter most for their bot - the functionality.


## Architecture

Project Duet is composed of two things:

- **Kaori** (`gateway/`) - This is where all the magic happens, it has basic command registration and maintains only what could have been implemented manually by a developer. It is written in Go to be flexible.

- **Kosei** (`library/`) - These are the Client API wrappers that implements the Kaori API. We assume that all Kosei-based clients are gRPC clients and servers, so we just need to query a specific route from Kaori.

## This is early stage!

Keep in mind a lot of this stuff is not yet in stone and things may break or change throughout the development. If you have any issues, please don't hesitate to report it.

## Contributing

For beginners, we encourage you use VSCode for this as we declared a prebuilt Docker environment for you, simply install the extension and go to your remotes screen.