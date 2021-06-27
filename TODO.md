## To Do

- java.util.Stream
    > see parts of branch wip-code-cleanup
    * [ ] ask in Discord
    * [ ] wait for answer in Discord
    * [ ] see TODOs in StringUtil
- synchronized refactor
    * [ ] rewrite LOCK object in Settings to use synchronized(this)
- Javadocs
    > NOTE: maybe use a screenshot of IntelliJ's render of some Javadoc to compare before/after
    * [ ] add missing char '#' in @links to methods
    * [ ] deal with @params without description delete or describe
    * [ ] remove dangling javadocs
    * [ ] use {@code} formatting where appropriate (param names)
    * [ ] use {@link} for types and such.
- Unit Tests
    * [ ] chatty.util.StringUtil.shortenTo(java.lang.String, int)
    * [ ] chatty.util.StringUtil.trimAll
    * [ ] Parser (commands)
    * [ ] ...

## In development

- JUnit 5
    * [x] Migrate to JUnit 5 (vintage, jupiter, etc)
    * [x] Add test reporting (lift from TRP/toschart)
    * [x] rename branch to "add-junit-5-support" --- less daunting than "Migrate to JUnit 5"
    * [x] open PR
    * [ ] wait
- notification-multiple-channels
    > Draft: After figuring out that field `Channel: ` in the `Connect` dialog
    > supports a comma-separated list of channels, I was surprised that
    > Notifications don't support it as well.  So here's implementation of
    > several channels matching for Notifications.
    * [x] write tests for serialization-deserialization _before_ implementation
    * [x] post config screenshot in discord
    * [x] update help HTML
    * [x] add tests for matchesChannel(null)
    * [x] add tests for Notification.channel(s) == null
    * [x] run locally for a while
    * [x] rebase
    * [x] open PR
    * [ ] wait
- java.time
    > tduva — 23/05/2021
    > Generally I don't really like refactoring unless an area is touched anyway or there's a good reason. What would be the advantage except it being cleaner?
    > andrybak — 23/05/2021
    > Because new API is based on immutable classes, you get thread safety for free, for example. Both java.util.Calendar and java.util.Date aren't thread safe.
    > tduva — 23/05/2021
    > I suppose it would work for most stuff, but would have to be careful not to change behavior, especially where user-customized timestamps are involved.
    > andrybak — 23/05/2021
    > Risk of breaking behaviour will be mitigated by generously adding tests.
    > ------
    > see parts of branch wip-code-cleanup
    * [x] ask in Discord
    * [x] wait for answer in Discord
    * [ ] add unit tests for DateTime
    * [ ] add unit tests for TBD
    * [ ] migrate from Calendar to Java 8 APIs

## Done

- Deploy scripts
    * [x] script to overwrite Chatty in ~/bin
    * [x] script to build Chatty
