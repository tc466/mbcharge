# mbcharge

Command line utility to control MacBook battery charging

Leaving lithium-ion batteries fully charged leads to faster aging and reduced
lifespan of the batteries. Apple introduced the [Optimized Battery Charging][optimized-battery-charing]
feature in macOS Big Sur to delay charging the battery past 80% until needed.
However, the feature relies on machine learning to generate schedules, and user
can't control when the battery starts and stops charging. This tool is for those who want more
manual control.

The utility allows turning on / off battery charging, and hold / unhold battery
at 80% for Apple Silicon MacBooks. Note that it does not work on older
generations of MacBooks (which uses a different mechanism to control battery
charging). Please use [bclm][bclm] or [AlDente][AlDente] instead for older
MacBooks.

## Prerequisites

You need the smc [command line tool][smc-command]
from [smcFanControl][smcFanControl]. A precompiled copy is provided in this
repository. Please download and put it in your $PATH together with the script.

## Usage

```
$ mbcharge enable
    Enables battery charging

$ mbcharge disable
    Disables battery charging

$ mbcharge hold
    Hold battery charge at 80%

$ mbcharge unhold
    Stop holding battery charge

$ mbcharge status
    Show battery charging and hold status
```

[optimized-battery-charing]: https://support.apple.com/guide/macbook-pro/charge-the-battery-apdbc13fd966/mac
[bclm]: https://github.com/zackelia/bclm
[AlDente]: https://github.com/davidwernhart/AlDente
[smc-command]: https://github.com/hholtmann/smcFanControl/tree/master/smc-command
[smcFanControl]: https://github.com/hholtmann/smcFanControl
