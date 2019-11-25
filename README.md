# evtx-data

## What's all this then?
Here you'll find a repository of community-contributed, publicly shareable windows event log message data stored in SQLite format. This data can be used with [dumpevtx](https://github.com/Velocidex/evtx/releases), which is the standalone CLI implementation of [Velociraptor](https://www.velocidex.com/)’s **parse_evtx()** VQL plugin. 

## Tell me more?
In addition to extracting data from Windows evtx files, the tool can also extract the descriptive event messages (that would normally only be viewable in Windows Event Viewer on the source computer) from the associated .dll files and then use these to enrich the data to make it more human-friendly and useful to security analysts and investigators.

The **dumpevtx** tool stores such data in SQLite database files which can be re-used when parsing offline evtx files (when the message dlls are not available) or for looking up more descriptive information on specific event IDs.

## Further reading

To understand more about the problems that **dumpevtx** solves and how it does so, we invite you to read the following article:
- [Windows Event Logs - What do they mean?](https://medium.com/velociraptor-ir/windows-event-logs-d8d8e615c9ca) 

You can also learn more over at the NSACyber WELM project:
- https://github.com/nsacyber/Windows-Event-Log-Messages