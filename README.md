# android-store-comparaison

This table does not attempt to document everything, because it's probably not feasible. It just look at some basic things.

✅ : ok
❌ : nok
⚠️ : warning


## Privacy/Security
| | F-Droid | Play Store | Accrescent | (Github/other) Release | Note |
|-|---|---|---|---|---|
| Trust repository signing key (must be reworded) | ❌ without RB / ✅ with RB | ❌ (since Play App signing) | ✅ (Depends on the dev setup, may be stored in github secret or other 3rd party service) | ⚠️ (Often stored in github secret) | Gives trust to the repository |
| Reproducible build (RB) (check automatically by 2 actors) | ✅ | ❌ | ❌ | ❌ | Reduces trust given to the build system and repository |
| Up to date build system | ✅ ([issues in 2022](https://gitlab.com/groups/fdroid/-/milestones/5#tab-issues)) | ✅ | ✅ | ✅ | Security consideration |
| Up to date app releases | ✅/⚠️ (4-5 days delayed, sometimes more when there is an issue) | ✅ (4/5 days delayed) | ✅ (Direct on dev upload, reviewed if there is a relevant change) | ✅ Direct | Security consideration |
| Up to date target API for client | ❌ ([WIP for basic](https://gitlab.com/fdroid/fdroidclient/-/merge_requests/1207)) | ✅ | ✅ | N/A | Security consideration |
| Up to date target API for apps | ❌ ([Waiting MR](https://gitlab.com/fdroid/fdroidclient/-/merge_requests/1214), then need to inform users when an app is installed with a low targetSdk) | ✅ ([requirement](https://developer.android.com/google/play/requirements/target-sdk)) | ✅ ([requirement](https://accrescent.app/docs/guide/publish/requirements.html#target-sdk)) | ❌ (No check) | Security consideration |
| SSL pinning (main repo) | ❌ | ✅ | ✅ | N/A (No client) | Security consideration - MITM for first install |
| Do unattended update | ❌ ([WIP for basic](https://gitlab.com/fdroid/fdroidclient/-/merge_requests/1216)) | ✅ | ✅ | ❌ | To keep up to date apps. Users must accept or be informed.
| Up to date signature scheme | ✅ (Up to v3) ([held on v1 in 2020](https://forum.f-droid.org/t/why-f-droid-is-still-using-apk-signature-scheme-v1/10602)) | ✅ | ✅ (Up to v3) | ❌ | Security
| Misleading permission approach (must be reworded) | ❌ (Too visible for common users, [Waiting MR](https://gitlab.com/fdroid/fdroidclient/-/merge_requests/1211)) | ✅ (Visible if you really look for them) | ✅ | ✅ | Misleading information |
| Disallows telemetry | ✅ (opt-out, foss) | ❌ | ❌ | ❌ | Privacy consideration |

\* Enforcing a suffix to the build is not listed here. [Google recommends, if the dev do not want cross-store update (if the flavors are different) to have different package Id OR a different signature.](https://developer.android.com/google/play/app-updates#multiple-stores).


## Other

| | F-Droid | Play Store | Accrescent | (Github/other) Release | Note |
|-|---|---|---|---|---|
| FOSS | ✅ | ❌ | ❌ | ❌ | Philosophical consideration |
| 3rd party repo with ability to self-host the backend | ✅ | ❌ | ❌ [intentionnaly](https://accrescent.app/faq#other-repos) | ✅ (any git/website) | Reduces power of the main team/ Allows alternative project |
| Feedback from the team (for instance when rejected) | ✅ | ❌ | ✅ | ✅ (dev publishes) | Relevant for many dev, can delay a lot app update |
| Update efficiency | ✅ (since JSON Merge Patch) | ✅ | ✅ | ❌ | Checking if update is available for all the installed app should be efficient. For instance, an RSS app for github releases may easily timeout with some apps. |
