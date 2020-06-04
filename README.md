# (No Title)

Project (Title HERE) is a gRPC-based bot gateway for Discord, it removes the need for you to implement sharding, event handling, etc. and focuses mostly on what matters the most: writing the functionality for your bot.

You can implement your own command engine using gRPC - and you don't need to worry about memory usage for it, it only needs to do two things, parse then send results.

## How it works

Project (Title HERE) is staying true to the microservices architecture, meaning you can split your bot's code into the gateway, the command engine, the cache, and the database.

This project solves the gateway part for you, as it sends context to your gRPC command backend and finds the suitable command for it.

## API

make sure you report all your commands as in first init, the gateway will perform a `GET` to `/reportcmds` in your command engine. Your command engine should be able to report all the cmds in an array then have them callable under the `/cmd/:cmdname` route.

More documentation coming soon.

## This is early stage!

Keep in mind a lot of this stuff is not yet in stone and things may break or change throughout the development. If you have any issues, please don't hesitate to report it.

## Contributing

For beginners, we encourage you use VSCode for this as we declared a prebuilt Docker environment for you, simply install the extension and go to your remotes screen.

For people who has dealt with Go before, standard Go rules apply here so if you're willing to help out please do so!