# mbcharge

Command line utility to control MacBook battery charging

Leaving lithium-ion batteries fully charged leads to faster aging of reduced
lifespan of the batteries. Apple introduced the [Optimized Battery Charging][optimized-battery-charing]
feature in macOS Big Sur to delay charging the battery past 80% until needed.
However, the feature relies on machine learning to generate schedules, and user
can't control when the battery starts and stops charging. This tool is for those who want more
manual control.

The utility allows turning on / off battery charging for MacBooks (including
MacBook Pro/Air with Apple Silicon). Note that it may not work on older
generations of MacBooks (which uses a different mechanism to control battery
charging). Please use [bclm][bclm] or [AlDente][AlDente] instead for older MacBooks.

## Prerequisites

You need the smc [command line tool][smc-command]
from [smcFanControl][smcFanControl]. Compile the command line tool and
place it in your $PATH.

## Usage

```
$ mbcharge on
    Enables battery charging

$ mbcharge off
    Disables battery charging

$ mbcharge status
    Show battery charging status
```

[optimized-battery-charing]: https://support.apple.com/guide/macbook-pro/charge-the-battery-apdbc13fd966/mac
[bclm]: https://github.com/zackelia/bclm
[AlDente]: https://github.com/davidwernhart/AlDente
[smc-command]: https://github.com/hholtmann/smcFanControl/tree/master/smc-command
[smcFanControl]: https://github.com/hholtmann/smcFanControl
