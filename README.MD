# Ultimate Mirror

The one-stop resources mirror

Powered by [MirrorEngine](https://github.com/NanoMeow/MirrorEngine).

A bot will update one resource every 2 hours, there are just over 80 resources,
so the mirror is updated about once a week.

## Motivation

This mirror is created as a response to
[this incidence](https://github.com/uBlockOrigin/uBlock-issues/issues/285).
Should a similar issue arises, we have everything we need to respond quickly
and effectively. More information can be found in the
[incidence response protocol](https://github.com/NanoAdblocker/NanoCore2#subresource-integrity-incidence-response-protocol).

## Content

Unless there is a need for intervention, the `/raw` directory will contain the
original unaltered or almost unaltered content downloaded from the origin
server. `!#include` directives may be rewritten to fit the file structure of
this mirror.

All files are downloaded over HTTPS with certificate validation.

Please open an issue with appropriate details if you think there is a
severe issue with the content of any mirrored files.

**For other filters related problems, please open issues in the
[NanoFilters](https://github.com/NanoAdblocker/NanoFilters) repository.**

## Truncate History

To keep the size of this repository under control, Git history can be
truncated. About a week worth of history should be kept just in case.

```Bash
git checkout --orphan temp <commit_hash>
git commit --message="Truncate history"
git rebase --onto temp <commit_hash> master
git branch --delete --force temp
git push --force
```

## License

Files mirrored here are under various open source or almost open source
licenses, more details can be found in the
[main manifest](https://github.com/NanoAdblocker/NanoCore2/blob/master/src/assets.json)
and the [include manifest](/config/include.json).

Note that some resources mirrored here prohibit commercial use.

Please open an issue with appropriate details if you think there is a problem
with licensing.
