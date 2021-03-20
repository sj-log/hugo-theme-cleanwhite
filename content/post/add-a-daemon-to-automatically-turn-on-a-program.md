---
title: "Add a Daemon to Automatically Turn on a Program"
date: 2020-08-28T11:49:14+09:00
hidden: false
draft: true
tags: [systemctl, Daemon, Redshift, Linux]
keywords: [Coding]
description: "log of failure but learned."
slug: ""
---

wanted to start the bluescreen blocking program 'redshift' every boot.
so downloaded through `sudo apt install redshift`. Then following stages I've tried and reached at the success implement.


## step by step

1. create a unit file at `/lib/systemd/system/redshift.service`

```
[Unit]
Description=Example systemd service.

[Service]
Type=simple
ExecStart=/bin/bash /usr/bin/redshift

[Install]
WantedBy=multi-user.target
```

2. gave it a permission with `sudo chmod +x redshift.service`

3. make it turning on every boot by `sudo systemctl enable redshift`

## troubleshooting

- `chmod 644 redshift.service` failed on activation the target service. 
Otherwise,`chmod +x foo.service` did work.

## Conclusion

but I found, daemon is not a solution to turn on 'redshift' every boot.
It goes looping then, explosively burst CPU.
So, It should not be done, but rather on `/.bashrc` to call once when terminal start.
That's far safe.

learned this.
1. `/etc/systemd/system/foo.service` is the target file to recoginize `systemctl`.
2. at the `ExecStart=/path/`, the `/path/` must be a file path, not a `command` like `redshift -O 3000`. Otherwise, it will looping and burst the cpu.

## reference

https://medium.com/@benmorel/creating-a-linux-service-with-systemd-611b5c8b91d6
https://www.linode.com/docs/quick-answers/linux/start-service-at-boot/

