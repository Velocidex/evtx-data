# NSACyber WELM data

This message files in this section were extracted from the information made publicly available by [NSA Cybersecurity's WELM](https://github.com/nsacyber/Windows-Event-Log-Messages) project. 

> The Windows Event Log Messages (WELM) tool retrieves the definitions of Windows Event Log messages embedded in binaries. The tool's output can be used to create an exhaustive list of event information for an operating system.

Data in the file below were extracted from the most recent dataset [WELM 2.3.0.0 and 04/06/2017](https://github.com/nsacyber/Windows-Event-Log-Messages/releases/tag/v2.3.0.0-20170406) dataset which is unfortunately a bit old, yet nonetheless still useful since many of the operating systems documented by the WELM tool are still in active use. The WELM project does not seem to be actively maintained.

The data was taken from the "new style" WELM extracts which they have named `events.csv` in their dataset.

> "Classic style" versus "new style". The "new style" metadata is retrieved using Windows event log APIs introduced in Windows Vista with the new event log system often referred to by its codename of Crimson. The "classic style" metadata is retrieved from the Windows registry for log metadata and source metadata and from text resources embedded in binaries for event metadata.

Windows XP only has "classic style" events and is therefore not listed below.

The SQLite db files have been named according to the WELM folder from which the event message information originated.

The WELM tool seems to not cover the more exotic locations where event messages can be found, however they do provide coverage of the core event message DLLs.

For convenience we have provided a combined WELM message database - `welm_combined.db`- which was produced by starting from the newest OS release files and sequentially adding data from the older ones. Through this process a great deal of deduplication can be observed. This process of merging means there may be inaccuracies since newer data would have taken precedence over older data, but Microsoft has at least has kept most core events consistent over the years, so this data should be 99% correct and useful for less stringent use cases. If you have access to live Windows systems you can use any of these files as a starting point and add to it using `dumpevtx.exe extract [filename].db`.