# android-store-comparaison

✅ : ok
❌ : nok
⚠️ : warning


## Privacy/Security
| | F-Droid | Play Store | Accrescent | (Github/other) Release | Note |
|-|---|---|---|---|---|
| Trust repository signing key | ❌ without RB / ✅ with RB | ❌ (since Play App signing) | ✅/⚠️ (Often stocked in github secret) | ⚠️ (Often stocked in github secret) | Gives trust to the repository |
| Reproducible build (RB) (check automatically by 2 actors) | ✅ | ❌ | ❌ | ❌ | Reduces trust given to the build system and repository |
| Up to date build system | ✅ ([issues in 2022](https://gitlab.com/groups/fdroid/-/milestones/5#tab-issues)) | ✅ | ✅ | ✅ | Security consideration |
| Up to date app releases | ✅/⚠️ (4-5 days delayed, sometimes more when there is an issue) | ✅ (4/5 days delayed) | ??? | ✅ Direct | Security consideration |
| Low target API for client | ❌ ([WIP for basic](https://gitlab.com/fdroid/fdroidclient/-/merge_requests/1207)) | ✅ | ✅ | N/A | Security consideration |
| Low target API for apps | ❌ ([Waiting MR](https://gitlab.com/fdroid/fdroidclient/-/merge_requests/1214)) | ✅ | ✅ | ❌ (No check) | Security consideration |
| SSL pinning (main repo) | ❌ | ✅ | ??? | N/A (No client) | Security consideration - MITM for first install |
| Do unattended update | ❌ ([WIP for basic](https://gitlab.com/fdroid/fdroidclient/-/merge_requests/1216)) | ??? | ??? | ❌ | To keep up to date apps. Users must accept or be informed.
| Up to date signature scheme | ✅/⚠️ Up to v3 ([held on v1 in 2020](https://forum.f-droid.org/t/why-f-droid-is-still-using-apk-signature-scheme-v1/10602)) | ✅ | ??? | ❌ | Security
| (???) Enforce suffix to the build | ❌ (for non-RB) | ❌ | ??? | N/A | [Google recommends, if the dev do not want cross-store update (if the flavors are different) to have different package Id OR a different signature.](https://developer.android.com/google/play/app-updates#multiple-stores), not relevant ? |
| Misleading permission approach | ❌ (Too visible for common users, [Waiting MR](https://gitlab.com/fdroid/fdroidclient/-/merge_requests/1211)) | ✅ (Visible if you really look for them) | ✅ | ✅ | Misleading information |
| Disallows telemetry | ✅ (opt-out, foss) | ❌ | ??? | ❌ | Privacy consideration |



## Other

| | F-Droid | Play Store | Accrescent | (Github/other) Release | Note |
|-|---|---|---|---|---|
| FOSS | ✅ | ❌ | ❌ | ❌ | Philosophical consideration |
| Self-hostable backend | ✅ | ❌ | ❌ | ✅ (any git/website) | Reduces power of the main team/ Allows alternative project |
| Feedback from the team (for instance when rejected) | ✅ | ❌ | ✅ (I guess) | ✅ (dev publishes) | Relevant for many dev, can delay a lot app update |
| Update efficiency | ✅ (since JSON Merge Patch) | ✅ | ??? | ❌ | Checking if update is available for all the installed app should be efficient. For instance, an RSS app for github releases may easily timeout with some apps. |
