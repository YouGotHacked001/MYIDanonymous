Changelog
=========

All notable changes to this project will be documented in this file.

## [3.5.0] - 2022-03-30
### Added

- **Add support for incoming edited posts** ([Gargron](https://www.okglobalcoinsg.com//pull/16697), [Gargron](https://www.okglobalcoinsg.com//pull/17727), [Gargron](https://www.okglobalcoinsg.com//pull/17728), [Gargron](https://www.okglobalcoinsg.com//pull/17320), [Gargron](https://www.okglobalcoinsg.com//pull/17404), [Gargron](https://www.okglobalcoinsg.com//pull/17390), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17335), [Gargron](https://www.okglobalcoinsg.com//pull/17696), [Gargron](https://www.okglobalcoinsg.com//pull/17745), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17740), [Gargron](https://www.okglobalcoinsg.com//pull/17697), [Gargron](https://www.okglobalcoinsg.com//pull/17648), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17531), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17499), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17498), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17380), [Gargron](https://www.okglobalcoinsg.com//pull/17373), [Gargron](https://www.okglobalcoinsg.com//pull/17334), [Gargron](https://www.okglobalcoinsg.com//pull/17333), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17699), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17748))
  - Previous versions remain available for perusal and comparison
  - People who reblogged a post are notified when it's edited
  - New REST APIs:
    - `PUT /api/v1/statuses/:id`
    - `GET /api/v1/statuses/:id/history`
    - `GET /api/v1/statuses/:id/source`
  - New streaming API event:
    - `status.update`
- **Add appeals for moderator decisions** ([Gargron](https://www.okglobalcoinsg.com//pull/17364), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17725), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17566), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17652), [Gargron](https://www.okglobalcoinsg.com//pull/17616), [Gargron](https://www.okglobalcoinsg.com//pull/17615), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17554), [Gargron](https://www.okglobalcoinsg.com//pull/17523))
  - All default moderator decisions now notify the affected user by e-mail
  - They now link to an appeal page instead of suggesting replying to the e-mail
  - They can now be found in account settings and not just e-mail
  - Users can submit one appeal within 20 days of the decision
  - Moderators can approve or reject the appeal
- **Add notifications for posts deleted by moderators** ([Gargron](https://www.okglobalcoinsg.com//pull/17204), [Gargron](https://www.okglobalcoinsg.com//pull/17668), [Gargron](https://www.okglobalcoinsg.com//pull/17746), [Gargron](https://www.okglobalcoinsg.com//pull/17679), [Gargron](https://www.okglobalcoinsg.com//pull/17487))
  - New, redesigned report view in admin UI
  - Common report actions now only take one click to complete
  - Deleting posts or marking as sensitive from report now notifies user
  - Reports can be categorized by reason and specific rules violated
  - The reasons are automatically cited in the notifications, except for spam
  - Marking posts as sensitive now federates using post editing
- **Add explore page with trending posts and links** ([Gargron](https://www.okglobalcoinsg.com//pull/17123), [Gargron](https://www.okglobalcoinsg.com//pull/17431), [Gargron](https://www.okglobalcoinsg.com//pull/16917), [Gargron](https://www.okglobalcoinsg.com//pull/17677), [Gargron](https://www.okglobalcoinsg.com//pull/16938), [Gargron](https://www.okglobalcoinsg.com//pull/17044), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16978), [Gargron](https://www.okglobalcoinsg.com//pull/16979), [tribela](https://www.okglobalcoinsg.com//pull/17066), [Gargron](https://www.okglobalcoinsg.com//pull/17072), [Gargron](https://www.okglobalcoinsg.com//pull/17403), [noiob](https://www.okglobalcoinsg.com//pull/17624), [mayaeh](https://www.okglobalcoinsg.com//pull/17755), [mayaeh](https://www.okglobalcoinsg.com//pull/17757), [Gargron](https://www.okglobalcoinsg.com//pull/17760), [mayaeh](https://www.okglobalcoinsg.com//pull/17762))
  - Hashtag trends algorithm is extended to work for posts and links
  - Links are only considered if they have an adequate preview card
  - Preview card generation has been improved to support structured data
  - Links can only trend if the publisher (domain) has been approved
  - Posts can only trend if the author has been approved
  - Individual approval and rejection for posts and links is also available
  - Moderators are notified about pending trends at most once every 2 hours
  - Posts and link trends are language-specific
  - Search page is redesigned into explore page in web UI
  - Discovery tab is coming soon in official iOS and Android apps
  - New REST APIs:
    - `GET /api/v1/trends/links`
    - `GET /api/v1/trends/statuses`
    - `GET /api/v1/trends/tags` (alias of `GET /api/v1/trends`)
    - `GET /api/v1/admin/trends/links`
    - `GET /api/v1/admin/trends/statuses`
    - `GET /api/v1/admin/trends/tags`
- **Add graphs and retention metrics to admin dashboard** ([Gargron](https://www.okglobalcoinsg.com//pull/16829), [Gargron](https://www.okglobalcoinsg.com//pull/17617), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17570), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16910), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16909), [mashirozx](https://www.okglobalcoinsg.com//pull/16884), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16854))
  - Dashboard shows more numbers with development over time
  - Other data such as most used interface languages and sign-up sources
  - User retention graph shows how many new users stick around
  - New REST APIs:
    - `POST /api/v1/admin/measures`
    - `POST /api/v1/admin/dimensions`
    - `POST /api/v1/admin/retention`
- Add `GET /api/v1/accounts/familiar_followers` to REST API ([Gargron](https://www.okglobalcoinsg.com//pull/17700))
- Add `POST /api/v1/accounts/:id/remove_from_followers` to REST API ([noellabo](https://www.okglobalcoinsg.com//pull/16864))
- Add `category` and `rule_ids` params to `POST /api/v1/reports` IN REST API ([Gargron](https://www.okglobalcoinsg.com//pull/17492), [Gargron](https://www.okglobalcoinsg.com//pull/17682), [Gargron](https://www.okglobalcoinsg.com//pull/17713))
  - `category` can be one of: `spam`, `violation`, `other` (default)
  - `rule_ids` must reference `rules` returned in `GET /api/v1/instance`
- Add global `lang` param to REST API ([Gargron](https://www.okglobalcoinsg.com//pull/17464), [Gargron](https://www.okglobalcoinsg.com//pull/17592))
- Add `types` param to `GET /api/v1/notifications` in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/17767))
- **Add notifications for moderators about new sign-ups** ([Gargron](https://www.okglobalcoinsg.com//pull/16953), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17629))
  - When a new user confirms e-mail, moderators receive a notification
  - New notification type:
    - `admin.sign_up`
- Add authentication history ([Gargron](https://www.okglobalcoinsg.com//pull/16408), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16428), [baby-gnu](https://www.okglobalcoinsg.com//pull/16654))
- Add ability to automatically delete old posts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16529), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17691), [tribela](https://www.okglobalcoinsg.com//pull/16653))
- Add ability to pin private posts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16954), [tribela](https://www.okglobalcoinsg.com//pull/17326), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17304), [MitarashiDango](https://www.okglobalcoinsg.com//pull/17647))
- Add ability to filter search results by author using `from:` syntax ([tribela](https://www.okglobalcoinsg.com//pull/16526))
- Add ability to delete canonical email blocks in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16644))
- Add ability to purge undeliverable domains in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16686), [tribela](https://www.okglobalcoinsg.com//pull/17210), [tribela](https://www.okglobalcoinsg.com//pull/17741), [tribela](https://www.okglobalcoinsg.com//pull/17209))
- Add ability to disable e-mail token authentication for specific users in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/16427))
- **Add ability to suspend accounts in batches in admin UI** ([Gargron](https://www.okglobalcoinsg.com//pull/17009), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17301), [Gargron](https://www.okglobalcoinsg.com//pull/17444))
  - New, redesigned accounts list in admin UI
  - Batch suspensions are meant to help clean up spam and bot accounts
  - They do not generate notifications
- Add ability to filter reports by origin of target account in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/16487))
- Add support for login through OpenID Connect ([chandrn7](https://www.okglobalcoinsg.com//pull/16221))
- Add lazy loading for emoji picker in web UI ([mashirozx](https://www.okglobalcoinsg.com//pull/16907), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17011))
- Add single option votes tooltip in polls in web UI ([Brawaru](https://www.okglobalcoinsg.com//pull/16849))
- Add confirmation modal when closing media edit modal with unsaved changes in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16518))
- Add hint about missing media attachment description in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/17845))
- Add support for fetching Create and Announce activities by URI in ActivityPub ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16383))
- Add `S3_FORCE_SINGLE_REQUEST` environment variable ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16866))
- Add `OMNIAUTH_ONLY` environment variable ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17288), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17345))
- Add `ES_USER` and `ES_PASS` environment variables for Elasticsearch authentication ([tribela](https://www.okglobalcoinsg.com//pull/16890))
- Add `CAS_SECURITY_ASSUME_EMAIL_IS_VERIFIED` environment variable ([baby-gnu](https://www.okglobalcoinsg.com//pull/16655))
- Add ability to pass specific domains to `tootctl accounts cull` ([tribela](https://www.okglobalcoinsg.com//pull/16511))
- Add `--by-uri` option to `tootctl domains purge` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16434))
- Add `--batch-size` option to `tootctl search deploy` ([aquarla](https://www.okglobalcoinsg.com//pull/17049))
- Add `--remove-orphans` option to `tootctl statuses remove` ([noellabo](https://www.okglobalcoinsg.com//pull/17067))

### Changed

- Change design of federation pages in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/17704), [noellabo](https://www.okglobalcoinsg.com//pull/17735), [Gargron](https://www.okglobalcoinsg.com//pull/17765))
- Change design of account cards in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/17689))
- Change `follow` scope to be covered by `read` and `write` scopes in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/17678))
- Change design of authorized applications page ([Gargron](https://www.okglobalcoinsg.com//pull/17656), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17686))
- Change e-mail domain blocks to block IPs dynamically ([Gargron](https://www.okglobalcoinsg.com//pull/17635), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17650), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17649))
- Change report modal to include category selection in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/17565), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17734), [Gargron](https://www.okglobalcoinsg.com//pull/17654), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17632))
- Change reblogs to not count towards hashtag trends anymore ([Gargron](https://www.okglobalcoinsg.com//pull/17501))
- Change languages to be listed under standard instead of native name in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/17485))
- Change routing paths to use usernames in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/16171), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16772), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16773), [mashirozx](https://www.okglobalcoinsg.com//pull/16793), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17060))
- Change list title input design in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17092))
- Change "Opt-in to profile directory" preference to be general discoverability preference ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16637))
- Change API rate limits to use /64 masking on IPv6 addresses ([tribela](https://www.okglobalcoinsg.com//pull/17588), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17600), [zunda](https://www.okglobalcoinsg.com//pull/17590))
- Change allowed formats for locally uploaded custom emojis to include GIF ([rgroothuijsen](https://www.okglobalcoinsg.com//pull/17706), [Gargron](https://www.okglobalcoinsg.com//pull/17759))
- Change error message when chosen password is too long ([rgroothuijsen](https://www.okglobalcoinsg.com//pull/17082))
- Change minimum required Elasticsearch version from 6 to 7 ([noellabo](https://www.okglobalcoinsg.com//pull/16915))

### Removed

- Remove profile directory link from main navigation panel in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/17688))
- **Remove language detection through cld3** ([Gargron](https://www.okglobalcoinsg.com//pull/17478), [ykzts](https://www.okglobalcoinsg.com//pull/17539), [Gargron](https://www.okglobalcoinsg.com//pull/17496), [Gargron](https://www.okglobalcoinsg.com//pull/17722))
  - cld3 is very inaccurate on short-form content even with unique alphabets
  - Post language can be overriden individually using `language` param
  - Otherwise, it defaults to the user's interface language
- Remove support for `OAUTH_REDIRECT_AT_SIGN_IN` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17287))
  - Use `OMNIAUTH_ONLY` instead
- Remove Keybase integration ([Gargron](https://www.okglobalcoinsg.com//pull/17045))
- Remove old columns and indexes ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17245), [Gargron](https://www.okglobalcoinsg.com//pull/16409), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17191))
- Remove shortcodes from newly-created media attachments ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16730), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16763))

### Deprecated

- `GET /api/v1/trends` → `GET /api/v1/trends/tags`
- OAuth `follow` scope → `read` and/or `write`
- `text` attribute on `DELETE /api/v1/statuses/:id` → `GET /api/v1/statuses/:id/source`

### Fixed

- Fix IDN domains not being rendered correctly in a few left-over places ([Gargron](https://www.okglobalcoinsg.com//pull/17848))
- Fix Sanskrit translation not being used in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17820))
- Fix Kurdish languages having the wrong language codes ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17812))
- Fix pghero making database schema suggestions ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17807))
- Fix encoding glitch in the OpenGraph description of a profile page ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17821))
- Fix web manifest not permitting PWA usage from alternate domains ([HolgerHuo](https://www.okglobalcoinsg.com//pull/16714))
- Fix not being able to edit media attachments for scheduled posts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17690))
- Fix subscribed relay activities being recorded as boosts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17571))
- Fix streaming API server error messages when JSON parsing fails not specifying the source ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17559))
- Fix browsers autofilling new password field with old password ([mashirozx](https://www.okglobalcoinsg.com//pull/17702))
- Fix text being invisible before fonts load in web UI ([tribela](https://www.okglobalcoinsg.com//pull/16330))
- Fix public profile pages of unconfirmed users being accessible ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17385), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17457))
- Fix nil error when trying to fetch key for signature verification ([Gargron](https://www.okglobalcoinsg.com//pull/17747))
- Fix null values being included in some indexes ([Gargron](https://www.okglobalcoinsg.com//pull/17711))
- Fix `POST /api/v1/emails/confirmations` not being available after sign-up ([Gargron](https://www.okglobalcoinsg.com//pull/17743))
- Fix rare race condition when reblogged post is deleted ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17693), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17730))
- Fix being able to add more than 4 hashtags to hashtag column in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/17729))
- Fix data integrity of featured tags ([Gargron](https://www.okglobalcoinsg.com//pull/17712))
- Fix performance of account timelines ([Gargron](https://www.okglobalcoinsg.com//pull/17709))
- Fix returning empty `<p>` tag for blank account `note` in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/17687))
- Fix leak of existence of otherwise inaccessible posts in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/17684))
- Fix not showing loading indicator when searching in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/17655))
- Fix media modal footer's “external link” not being a link ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17561))
- Fix reply button on media modal not giving focus to compose form ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17626))
- Fix some media attachments being converted with too high framerates ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17619))
- Fix sign in token and warning emails failing to send when contact e-mail address is malformed ([helloworldstack](https://www.okglobalcoinsg.com//pull/17589))
- Fix opening the emoji picker scrolling the single-column view to the top ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17579))
- Fix edge case where settings/admin page sidebar would be incorrectly hidden ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17580))
- Fix performance of server-side filtering ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17575))
- Fix privacy policy link not being visible on small screens ([Gargron](https://www.okglobalcoinsg.com//pull/17533))
- Fix duplicate accounts when searching by IP range in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/17524), [tribela](https://www.okglobalcoinsg.com//pull/17150))
- Fix error when performing a batch action on posts in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17532))
- Fix deletes not being signed in authorized fetch mode ([Gargron](https://www.okglobalcoinsg.com//pull/17484))
- Fix Undo Announce sometimes inlining the originally Announced status ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17516))
- Fix localization of cold-start follow recommendations ([Gargron](https://www.okglobalcoinsg.com//pull/17479), [Gargron](https://www.okglobalcoinsg.com//pull/17486))
- Fix replies collection incorrectly looping ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17462))
- Fix errors when multiple Delete are received for a given actor ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17460))
- Fixed prototype pollution bug and only allow trusted origin ([r0hanSH](https://www.okglobalcoinsg.com//pull/17420))
- Fix text being incorrectly pre-selected in composer textarea on /share ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17339))
- Fix SMTP_ENABLE_STARTTLS_AUTO/SMTP_TLS/SMTP_SSL environment variables don't work ([kgtkr](https://www.okglobalcoinsg.com//pull/17216))
- Fix media upload specific rate limits only being applied to v1 endpoint in REST API ([tribela](https://www.okglobalcoinsg.com//pull/17272))
- Fix media descriptions not being used for client-side filtering ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17206))
- Fix cold-start follow recommendation favouring older accounts due to wrong sorting ([noellabo](https://www.okglobalcoinsg.com//pull/17126))
- Fix not redirect to the right page after authenticating with WebAuthn ([heguro](https://www.okglobalcoinsg.com//pull/17098))
- Fix searching for additional hashtags in hashtag column ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17054))
- Fix color of hashtag column settings inputs ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17058))
- Fix performance of `tootctl statuses remove` ([noellabo](https://www.okglobalcoinsg.com//pull/17052))
- Fix `tootctl accounts cull` not excluding domains on timeouts and certificate issues ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16433))
- Fix 404 error when filtering admin action logs by non-existent target account ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16643))
- Fix error when accessing streaming API without any OAuth scopes ([Brawaru](https://www.okglobalcoinsg.com//pull/16823))
- Fix follow request count not updating when new follow requests arrive over streaming API in web UI ([matildepark](https://www.okglobalcoinsg.com//pull/16652))
- Fix error when unsuspending a local account ([HolgerHuo](https://www.okglobalcoinsg.com//pull/16605))
- Fix crash when a notification contains a not yet processed media attachment in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16573))
- Fix wrong color of download button in audio player in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16572))
- Fix notes for others accounts not being deleted when an account is deleted ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16579))
- Fix error when logging occurrence of unsupported video file ([noellabo](https://www.okglobalcoinsg.com//pull/16581))
- Fix wrong elements in trends widget being hidden on smaller screens in web UI ([tribela](https://www.okglobalcoinsg.com//pull/16570))
- Fix link to about page being displayed in limited federation mode ([weex](https://www.okglobalcoinsg.com//pull/16432))
- Fix styling of boost button in media modal not reflecting ability to boost ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16387))
- Fix OCR failure when erroneous lang data is in cache ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16386))
- Fix downloading media from blocked domains in `tootctl media refresh` ([tribela](https://www.okglobalcoinsg.com//pull/16914))
- Fix login form being displayed on landing page when already logged in ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17348))
- Fix polling for media processing status too frequently in web UI ([tribela](https://www.okglobalcoinsg.com//pull/17271))
- Fix hashtag autocomplete overriding user-typed case ([weex](https://www.okglobalcoinsg.com//pull/16460))
- Fix WebAuthn authentication setup to not prompt for PIN ([truongnmt](https://www.okglobalcoinsg.com//pull/16545))

### Security

- Fix being able to post URLs longer than 4096 characters ([Gargron](https://www.okglobalcoinsg.com//pull/17908))
- Fix being able to bypass e-mail restrictions ([Gargron](https://www.okglobalcoinsg.com//pull/17909))

## [3.4.6] - 2022-02-03
### Fixed

- Fix `mastodon:webpush:generate_vapid_key` task requiring a functional environment ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17338))
- Fix spurious errors when receiving an Add activity for a private post ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17425))

### Security

- Fix error-prone SQL queries ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15828))
- Fix not compacting incoming signed JSON-LD activities ([puckipedia](https://www.okglobalcoinsg.com//pull/17426), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/17428)) (CVE-2022-24307)
- Fix insufficient sanitization of report comments ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17430))
- Fix stop condition of a Common Table Expression ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17427))
- Disable legacy XSS filtering ([Wonderfall](https://www.okglobalcoinsg.com//pull/17289))

## [3.4.5] - 2022-01-31
### Added

- Add more advanced migration tests ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17393))
- Add github workflow to build Docker images ([unasuke](https://www.okglobalcoinsg.com//pull/16973), [Gargron](https://www.okglobalcoinsg.com//pull/16980), [Gargron](https://www.okglobalcoinsg.com//pull/17000))

### Fixed

- Fix some old migrations failing when skipping releases ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17394))
- Fix migrations script failing in certain edge cases ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17398))
- Fix Docker build ([tribela](https://www.okglobalcoinsg.com//pull/17188))
- Fix Ruby 3.0 dependencies ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16723))
- Fix followers synchronization mechanism ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16510))

## [3.4.4] - 2021-11-26
### Fixed

- Fix error when suspending user with an already blocked canonical email ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17036))
- Fix overflow of long profile fields in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17010))
- Fix confusing error when WebFinger request returns empty document ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16986))
- Fix upload of remote media with OpenStack Swift sometimes failing ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16998))
- Fix logout link not working in Safari ([noellabo](https://www.okglobalcoinsg.com//pull/16574))
- Fix “open” link of media modal not closing modal in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16524))
- Fix replying from modal in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16516))
- Fix `mastodon:setup` command crashing in some circumstances ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16976))

### Security

- Fix filtering DMs from non-followed users ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17042))
- Fix handling of recursive toots in WebUI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/17041))

## [3.4.3] - 2021-11-06
### Fixed

- Fix login being broken due to inaccurately applied backport fix in 3.4.2 ([Gargron](https://www.okglobalcoinsg.com//commit/5c47a18c8df3231aa25c6d1f140a71a7fac9cbf9))

## [3.4.2] - 2021-11-06
### Added

- Add `configuration` attribute to `GET /api/v1/instance` ([Gargron](https://www.okglobalcoinsg.com//pull/16485))

### Fixed

- Fix handling of back button with modal windows in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16499))
- Fix pop-in player when author has long username in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16468))
- Fix crash when a status with a playing video gets deleted in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16384))
- Fix crash with Microsoft Translate in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16525))
- Fix PWA not being usable from alternate domains ([HolgerHuo](https://www.okglobalcoinsg.com//pull/16714))
- Fix locale-specific number rounding errors ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16469))
- Fix scheduling a status decreasing status count ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16791))
- Fix user's canonical email address being blocked when user deletes own account ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16503))
- Fix not being able to suspend users that already have their canonical e-mail blocked ([Gargron](https://www.okglobalcoinsg.com//pull/16455))
- Fix anonymous access to outbox not being cached by the reverse proxy ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16458))
- Fix followers synchronization mechanism not working when URI has empty path ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16744))
- Fix serialization of counts in REST API when user hides their network ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16418))
- Fix inefficiencies in auto-linking code ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16506))
- Fix `tootctl self-destruct` not sending delete activities for recently-suspended accounts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16688))
- Fix suspicious sign-in e-mail text being out of date ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16690))
- Fix some frameworks being unnecessarily loaded ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16725))
- Fix canonical e-mail blocks missing foreign key constraints ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16448))
- Fix inconsistent order on account's statuses page in admin UI ([tribela](https://www.okglobalcoinsg.com//pull/16937))
- Fix media from blocked domains being redownloaded by `tootctl media refresh` ([tribela](https://www.okglobalcoinsg.com//pull/16914))
- Fix `mastodon:setup` generated env-file syntax ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16896))
- Fix link previews being incorrectly generated from earlier links ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16885))
- Fix wrong `to`/`cc` values for remote groups in ActivityPub ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16700))
- Fix mentions with non-ascii TLDs not being processed ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16689))
- Fix authentication failures halfway through a sign-in attempt ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16607), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16792))
- Fix suspended accounts statuses being merged back into timelines ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16628))
- Fix crash when encountering invalid account fields ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16598))
- Fix invalid blurhash handling for remote activities ([noellabo](https://www.okglobalcoinsg.com//pull/16583))
- Fix newlines being added to account notes when an account moves ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16415), [noellabo](https://www.okglobalcoinsg.com//pull/16576))
- Fix crash when creating an announcement with links ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16941))
- Fix logging out from one browser logging out all other sessions ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16943))

### Security

- Fix user notes not having a length limit ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16942))
- Fix revoking a specific session not working ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16943))

## [3.4.1] - 2021-06-03
### Added

- Add new emoji assets from Twemoji 13.1.0 ([Gargron](https://www.okglobalcoinsg.com//pull/16345))

### Fixed

- Fix some ActivityPub identifiers in server actor outbox ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16343))
- Fix custom CSS path setting cookies and being uncacheable due to it ([tribela](https://www.okglobalcoinsg.com//pull/16314))
- Fix unread notification count when polling in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16272))
- Fix health check not being accessible through localhost ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16270))
- Fix some redis locks auto-releasing too fast ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16276), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16291))
- Fix e-mail confirmations API not working correctly ([Gargron](https://www.okglobalcoinsg.com//pull/16348))
- Fix migration script not being able to run if it fails midway ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16312))
- Fix account deletion sometimes failing because of optimistic locks ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16317))
- Fix deprecated slash as division in SASS files ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16347))
- Fix `tootctl search deploy` compatibility error on Ruby 3 ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16346))
- Fix mailer jobs for deleted notifications erroring out ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16294))

## [3.4.0] - 2021-05-16
### Added

- **Add follow recommendations for onboarding** ([Gargron](https://www.okglobalcoinsg.com//pull/15945), [Gargron](https://www.okglobalcoinsg.com//pull/16161), [Gargron](https://www.okglobalcoinsg.com//pull/16060), [Gargron](https://www.okglobalcoinsg.com//pull/16077), [Gargron](https://www.okglobalcoinsg.com//pull/16078), [Gargron](https://www.okglobalcoinsg.com//pull/16160), [Gargron](https://www.okglobalcoinsg.com//pull/16079), [noellabo](https://www.okglobalcoinsg.com//pull/16044), [noellabo](https://www.okglobalcoinsg.com//pull/16045), [Gargron](https://www.okglobalcoinsg.com//pull/16152), [Gargron](https://www.okglobalcoinsg.com//pull/16153), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16082), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16173), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16159), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16189))
  - Tutorial on first web UI launch has been replaced with follow suggestions
  - Follow suggestions take user locale into account and are a mix of accounts most followed by currently active local users, and accounts that wrote the most shared/favourited posts in the last 30 days
  - Only accounts that have opted-in to being discoverable from their profile settings, and that do not require follow requests, will be suggested
  - Moderators can review suggestions for every supported locale and suppress specific suggestions from appearing and admins can ensure certain accounts always show up in suggestions from the settings area
  - New users no longer automatically follow admins
- **Add server rules** ([Gargron](https://www.okglobalcoinsg.com//pull/15769), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15778))
  - Admins can create and edit itemized server rules
  - They are available through the REST API and on the about page
- **Add canonical e-mail blocks for suspended accounts** ([Gargron](https://www.okglobalcoinsg.com//pull/16049))
  - Normally, people can make multiple accounts using the same e-mail address using the `+` trick or by inserting or removing `.` characters from the first part of their address
  - Once an account is suspended, it will no longer be possible for the e-mail address used by that account to be used for new sign-ups in any of its forms
- Add management of delivery availability in admin UI ([noellabo](https://www.okglobalcoinsg.com//pull/15771))
- **Add system checks to dashboard in admin UI** ([Gargron](https://www.okglobalcoinsg.com//pull/15989), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15954), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16002))
  - The dashboard will now warn you if you some Sidekiq queues are not being processed, if you have not defined any server rules, or if you forgot to run database migrations from the latest Mastodon upgrade
- Add inline description of moderation actions in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15792))
- Add "recommended" label to activity/peers API toggles in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/16081))
- Add joined date to profiles in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/16169), [rinsuki](https://www.okglobalcoinsg.com//pull/16186))
- Add transition to media modal background in web UI ([mkljczk](https://www.okglobalcoinsg.com//pull/15843))
- Add option to opt-out of unread notification markers in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15842))
- Add borders to 📱, 🚲, and 📲 emojis in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15794), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16035))
- Add dropdown for boost privacy in boost confirmation modal in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15704))
- Add support for Ruby 3.0 ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16046), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16174))
- Add `Message-ID` header to outgoing emails ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16076))
  - Some e-mail spam filters penalize e-mails that have a `Message-ID` header that uses a different domain name than the sending e-mail address. Now, the same domain will be used
- Add `af`, `gd` and `si` locales ([Gargron](https://www.okglobalcoinsg.com//pull/16090))
- Add guard against DNS rebinding attacks ([noellabo](https://www.okglobalcoinsg.com//pull/16087), [noellabo](https://www.okglobalcoinsg.com//pull/16095))
- Add HTTP header to explicitly opt-out of FLoC by default ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16036))
- Add missing push notification title for polls and statuses ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15929), [mkljczk](https://www.okglobalcoinsg.com//pull/15564), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15931))
- Add `POST /api/v1/emails/confirmations` to REST API ([Gargron](https://www.okglobalcoinsg.com//pull/15816), [Gargron](https://www.okglobalcoinsg.com//pull/15949))
  - This method allows an app through which a user signed-up to request a new confirmation e-mail to be sent, or to change the e-mail of the account before it is confirmed
- Add `GET /api/v1/accounts/lookup` to REST API ([Gargron](https://www.okglobalcoinsg.com//pull/15740), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15750))
  - This method allows to quickly convert a username of a known account to an ID that can be used with the REST API, or to check if a username is available
  for sign-up
- Add `policy` param to `POST /api/v1/push/subscriptions` in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/16040))
  - This param allows an app to control from whom notifications should be delivered as push notifications to the app
- Add `details` to error response for `POST /api/v1/accounts` in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/15803))
  - This attribute allows an app to display more helpful information to the user about why the sign-up did not succeed
- Add `SIDEKIQ_REDIS_URL` and related environment variables to optionally use a separate Redis server for Sidekiq ([noellabo](https://www.okglobalcoinsg.com//pull/16188))

### Changed

- Change trending hashtags to be affected be reblogs ([Gargron](https://www.okglobalcoinsg.com//pull/16164))
  - Previously, only original posts contributed to a hashtag's trending score
  - Now, reblogs of posts will also contribute to that hashtag's trending score
- Change e-mail confirmation link to always redirect to web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16151))
- Change log level of worker lifecycle to WARN in streaming API ([Gargron](https://www.okglobalcoinsg.com//pull/16110))
  - Since running with INFO log level in production is not always desirable, it is easy to miss when a worker is shutdown and a new one is started
- Change the nouns "toot" and "status" to "post" in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/16080), [Gargron](https://www.okglobalcoinsg.com//pull/16089))
  - To be clear, the button still says "Toot!"
- Change order of dropdown menu on posts to be more intuitive in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/15647))
- Change description of keyboard shortcuts in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/16129))
- Change option labels on edit profile page ([Gargron](https://www.okglobalcoinsg.com//pull/16041))
  - "Lock account" is now "Require follow requests"
  - "List this account on the directory" is now "Suggest account to others"
  - "Hide your network" is now "Hide your social graph"
- Change newly generated account IDs to not be enumerable ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15844))
- Change Web Push API deliveries to use request pooling ([Gargron](https://www.okglobalcoinsg.com//pull/16014))
- Change multiple mentions with same username to render with domain ([Gargron](https://www.okglobalcoinsg.com//pull/15718), [noellabo](https://www.okglobalcoinsg.com//pull/16038))
  - When a post contains mentions of two or more users who have the same username, but on different domains, render their names with domain to help disambiguate them
  - Always render the domain of usernames used in profile metadata
- Change health check endpoint to reveal less information ([Gargron](https://www.okglobalcoinsg.com//pull/15988))
- Change account counters to use upsert (requires Postgres >= 9.5) ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15913))
- Change `mastodon:setup` to not call `assets:precompile` in Docker ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13942))
- **Change max. image dimensions to 1920x1080px (1080p)** ([Gargron](https://www.okglobalcoinsg.com//pull/15690))
  - Previously, this was 1280x1280px
  - This is the amount of pixels that original images get downsized to
- Change custom emoji to be animated when hovering container in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15637))
- Change streaming API from deprecated ClusterWS/cws to ws ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15932))
- Change systemd configuration to add sandboxing features ([Izorkin](https://www.okglobalcoinsg.com//pull/15937), [Izorkin](https://www.okglobalcoinsg.com//pull/16103), [Izorkin](https://www.okglobalcoinsg.com//pull/16127))
- Change nginx configuration to make running Onion service easier ([cohosh](https://www.okglobalcoinsg.com//pull/15498))
- Change Helm configuration ([dunn](https://www.okglobalcoinsg.com//pull/15722), [dunn](https://www.okglobalcoinsg.com//pull/15728), [dunn](https://www.okglobalcoinsg.com//pull/15748), [dunn](https://www.okglobalcoinsg.com//pull/15749), [dunn](https://www.okglobalcoinsg.com//pull/15767))
- Change Docker configuration ([SuperSandro2000](https://www.okglobalcoinsg.com//pull/10823), [mashirozx](https://www.okglobalcoinsg.com//pull/15978))

### Removed

- Remove PubSubHubbub-related columns from accounts table ([Gargron](https://www.okglobalcoinsg.com//pull/16170), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15857))
- Remove dependency on @babel/plugin-proposal-class-properties ([ykzts](https://www.okglobalcoinsg.com//pull/16155))
- Remove dependency on pluck_each gem ([Gargron](https://www.okglobalcoinsg.com//pull/16012))
- Remove spam check and dependency on nilsimsa gem ([Gargron](https://www.okglobalcoinsg.com//pull/16011))
- Remove MySQL-specific code from Mastodon::MigrationHelpers ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15924))
- Remove IE11 from supported browsers target ([gol-cha](https://www.okglobalcoinsg.com//pull/15779))

### Fixed

- Fix "You might be interested in" flashing while searching in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/16162))
- Fix display of posts without text content in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15665))
- Fix Google Translate breaking web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15610), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15611))
- Fix web UI crashing when SVG support is disabled ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15809))
- Fix web UI crash when a status opened in the media modal is deleted ([kaias1jp](https://www.okglobalcoinsg.com//pull/15701))
- Fix OCR language data failing to load in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15519))
- Fix footer links not being clickable in Safari in web UI ([noellabo](https://www.okglobalcoinsg.com//pull/15496))
- Fix autofocus/autoselection not working on mobile in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15555), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15985))
- Fix media redownload worker retrying on unexpected response codes ([Gargron](https://www.okglobalcoinsg.com//pull/16111))
- Fix thread resolve worker retrying when status no longer exists ([Gargron](https://www.okglobalcoinsg.com//pull/16109))
- Fix n+1 queries when rendering statuses in REST API ([abcang](https://www.okglobalcoinsg.com//pull/15641))
- Fix n+1 queries when rendering notifications in REST API ([abcang](https://www.okglobalcoinsg.com//pull/15640))
- Fix delete of local reply to local parent not being forwarded ([Gargron](https://www.okglobalcoinsg.com//pull/16096))
- Fix remote reporters not receiving suspend/unsuspend activities ([Gargron](https://www.okglobalcoinsg.com//pull/16050))
- Fix understanding (not fully qualified) `as:Public` and `Public` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15948))
- Fix actor update not being distributed on profile picture deletion ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15461))
- Fix processing of incoming Delete activities ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16084))
- Fix processing of incoming Block activities ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15546))
- Fix processing of incoming Update activities of unknown accounts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15514))
- Fix URIs of repeat follow requests not being recorded ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15662))
- Fix error on requests with no `Digest` header ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15782))
- Fix activity object not requiring signature in secure mode ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15592))
- Fix database serialization failure returning HTTP 500 ([Gargron](https://www.okglobalcoinsg.com//pull/16101))
- Fix media processing getting stuck on too much stdin/stderr ([Gargron](https://www.okglobalcoinsg.com//pull/16136))
- Fix some inefficient array manipulations ([007lva](https://www.okglobalcoinsg.com//pull/15513), [007lva](https://www.okglobalcoinsg.com//pull/15527))
- Fix some inefficient regex matching ([007lva](https://www.okglobalcoinsg.com//pull/15528))
- Fix some inefficient SQL queries ([abcang](https://www.okglobalcoinsg.com//pull/16104), [abcang](https://www.okglobalcoinsg.com//pull/16106), [abcang](https://www.okglobalcoinsg.com//pull/16105))
- Fix trying to fetch key from empty URI when verifying HTTP signature ([Gargron](https://www.okglobalcoinsg.com//pull/16100))
- Fix `tootctl maintenance fix-duplicates` failures ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15923), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15515))
- Fix error when removing status caused by race condition ([Gargron](https://www.okglobalcoinsg.com//pull/16099))
- Fix blocking someone not clearing up list feeds ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16205))
- Fix misspelled URLs character counting ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15382))
- Fix Sidekiq hanging forever due to a Resolv bug in Ruby 2.7.3 ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16157))
- Fix edge case where follow limit interferes with accepting a follow ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/16098))
- Fix inconsistent lead text style in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/16052), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/16086))
- Fix reports of already suspended accounts being recorded ([Gargron](https://www.okglobalcoinsg.com//pull/16047))
- Fix sign-up restrictions based on IP addresses not being enforced ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15607))
- Fix YouTube embeds failing due to YouTube serving wrong OEmbed URLs ([Gargron](https://www.okglobalcoinsg.com//pull/15716))
- Fix error when rendering public pages with media without meta ([Gargron](https://www.okglobalcoinsg.com//pull/16112))
- Fix misaligned logo on follow button on public pages ([noellabo](https://www.okglobalcoinsg.com//pull/15458))
- Fix video modal not working on public pages ([noellabo](https://www.okglobalcoinsg.com//pull/15469))
- Fix race conditions on account migration creation ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15597))
- Fix not being able to change world filter expiration back to “Never” ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15858))
- Fix `.env.vagrant` not setting `RAILS_ENV` variable ([chandrn7](https://www.okglobalcoinsg.com//pull/15709))
- Fix error when muting users with `duration` in REST API ([Tak](https://www.okglobalcoinsg.com//pull/15516))
- Fix border padding on front page in light theme ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15926))
- Fix wrong URL to custom CSS when `CDN_HOST` is used ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15927))
- Fix `tootctl accounts unfollow` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15639))
- Fix `tootctl emoji import` wasting time on MacOS shadow files ([cortices](https://www.okglobalcoinsg.com//pull/15430))
- Fix `tootctl emoji import` not treating shortcodes as case-insensitive ([angristan](https://www.okglobalcoinsg.com//pull/15738))
- Fix some issues with SAML account creation ([Gargron](https://www.okglobalcoinsg.com//pull/15222), [kaiyou](https://www.okglobalcoinsg.com//pull/15511))
- Fix MX validation applying for explicitly allowed e-mail domains ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15930))
- Fix share page not using configured custom mascot ([tribela](https://www.okglobalcoinsg.com//pull/15687))
- Fix instance actor not being automatically created if it wasn't seeded properly ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15693))
- Fix HTTPS enforcement preventing Mastodon from being run as an Onion service ([cohosh](https://www.okglobalcoinsg.com//pull/15560), [jtracey](https://www.okglobalcoinsg.com//pull/15741), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15712), [cohosh](https://www.okglobalcoinsg.com//pull/15725))
- Fix app name, website and redirect URIs not having a maximum length ([Gargron](https://www.okglobalcoinsg.com//pull/16042))

## [3.3.0] - 2020-12-27
### Added

- **Add hotkeys for audio/video control in web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/15158), [Gargron](https://www.okglobalcoinsg.com//pull/15198))
  - `Space` and `k` to toggle playback
  - `m` to toggle mute
  - `f` to toggle fullscreen
  - `j` and `l` to go back and forward by 10 seconds
  - `.` and `,` to go back and forward by a frame (video only)
- Add expand/compress button on media modal in web UI ([mashirozx](https://www.okglobalcoinsg.com//pull/15068), [mashirozx](https://www.okglobalcoinsg.com//pull/15088), [mashirozx](https://www.okglobalcoinsg.com//pull/15094))
- Add border around 🕺 emoji in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14769))
- Add border around 🐞 emoji in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14712))
- Add home link to the getting started column when home isn't mounted ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14707))
- Add option to disable swiping motions across the web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13885))
- **Add pop-out player for audio/video in web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/14870), [Gargron](https://www.okglobalcoinsg.com//pull/15157), [Gargron](https://www.okglobalcoinsg.com//pull/14915), [noellabo](https://www.okglobalcoinsg.com//pull/15309))
  - Continue watching/listening when you scroll away
  - Action bar to interact with/open toot from the pop-out player
- Add unread notification markers in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14818), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14960), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14954), [noellabo](https://www.okglobalcoinsg.com//pull/14897), [noellabo](https://www.okglobalcoinsg.com//pull/14907))
- Add paragraph about browser add-ons when encountering errors in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14801))
- Add import and export for bookmarks ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14956))
- Add cache buster feature for media files ([Gargron](https://www.okglobalcoinsg.com//pull/15155))
  - If you have a proxy cache in front of object storage, deleted files will persist until the cache expires
  - If enabled, cache buster will make a special request to the proxy to signal a cache reset
- Add duration option to the mute function ([aquarla](https://www.okglobalcoinsg.com//pull/13831))
- Add replies policy option to the list function ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9205), [trwnh](https://www.okglobalcoinsg.com//pull/15304))
- Add `og:published_time` OpenGraph tags on toots ([nornagon](https://www.okglobalcoinsg.com//pull/14865))
- **Add option to be notified when a followed user posts** ([Gargron](https://www.okglobalcoinsg.com//pull/13546), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14896), [Gargron](https://www.okglobalcoinsg.com//pull/14822))
  - If you don't want to miss a toot, click the bell button!
- Add client-side validation in password change forms ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14564))
- Add client-side validation in the registration form ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14560), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14599))
- Add support for Gemini URLs ([joshleeb](https://www.okglobalcoinsg.com//pull/15013))
- Add app shortcuts to web app manifest ([mkljczk](https://www.okglobalcoinsg.com//pull/15234))
- Add WebAuthn as an alternative 2FA method ([santiagorodriguez96](https://www.okglobalcoinsg.com//pull/14466), [jiikko](https://www.okglobalcoinsg.com//pull/14806))
- Add honeypot fields and minimum fill-out time for sign-up form ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15276))
- Add icon for mutual relationships in relationship manager ([noellabo](https://www.okglobalcoinsg.com//pull/15149))
- Add follow selected followers button in relationship manager ([noellabo](https://www.okglobalcoinsg.com//pull/15148))
- **Add subresource integrity for JS and CSS assets** ([Gargron](https://www.okglobalcoinsg.com//pull/15096))
  - If you use a CDN for static assets (JavaScript, CSS, and so on), you have to trust that the CDN does not modify the assets maliciously
  - Subresource integrity compares server-generated asset digests with what's actually served from the CDN and prevents such attacks
- Add `ku`, `sa`, `sc`, `zgh` to available locales ([ykzts](https://www.okglobalcoinsg.com//pull/15138))
- Add ability to force an account to mark media as sensitive ([noellabo](https://www.okglobalcoinsg.com//pull/14361))
- **Add ability to block access or limit sign-ups from chosen IPs** ([Gargron](https://www.okglobalcoinsg.com//pull/14963), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15263))
  - Add rules for IPs or CIDR ranges that automatically expire after a configurable amount of time
  - Choose the severity of the rule, either blocking all access or merely limiting sign-ups
- **Add support for reversible suspensions through ActivityPub** ([Gargron](https://www.okglobalcoinsg.com//pull/14989))
  - Servers can signal that one of their accounts has been suspended
  - During suspension, the account can only delete its own content
  - A reversal of the suspension can be signalled the same way
  - A local suspension always overrides a remote one
- Add indication to admin UI of whether a report has been forwarded ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13237))
- Add display of reasons for joining of an account in admin UI ([mashirozx](https://www.okglobalcoinsg.com//pull/15265))
- Add option to obfuscate domain name in public list of domain blocks ([Gargron](https://www.okglobalcoinsg.com//pull/15355))
- Add option to make reasons for joining required on sign-up ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15326), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15358), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15385), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15405))
- Add ActivityPub follower synchronization mechanism ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14510), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15026))
- Add outbox attribute to instance actor ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14721))
- Add featured hashtags as an ActivityPub collection ([Gargron](https://www.okglobalcoinsg.com//pull/11595), [noellabo](https://www.okglobalcoinsg.com//pull/15277))
- Add support for dereferencing objects through bearcaps ([Gargron](https://www.okglobalcoinsg.com//pull/14683), [noellabo](https://www.okglobalcoinsg.com//pull/14981))
- Add `S3_READ_TIMEOUT` environment variable ([tateisu](https://www.okglobalcoinsg.com//pull/14952))
- Add `ALLOWED_PRIVATE_ADDRESSES` environment variable ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14722))
- Add `--fix-permissions` option to `tootctl media remove-orphans` ([Gargron](https://www.okglobalcoinsg.com//pull/14383), [uist1idrju3i](https://www.okglobalcoinsg.com//pull/14715))
- Add `tootctl accounts merge` ([Gargron](https://www.okglobalcoinsg.com//pull/15201), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15264), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15256))
  - Has someone changed their domain or subdomain thereby creating two accounts where there should be one?
  - This command will fix it on your end
- Add `tootctl maintenance fix-duplicates` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14860), [Gargron](https://www.okglobalcoinsg.com//pull/15223), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15373))
  - Index corruption in the database?
  - This command is for you
- **Add support for managing multiple stream subscriptions in a single connection** ([Gargron](https://www.okglobalcoinsg.com//pull/14524), [Gargron](https://www.okglobalcoinsg.com//pull/14566), [mfmfuyu](https://www.okglobalcoinsg.com//pull/14859), [zunda](https://www.okglobalcoinsg.com//pull/14608))
  - Previously, getting live updates for multiple timelines required opening a HTTP or WebSocket connection for each
  - More connections means more resource consumption on both ends, not to mention the (ever so slight) delay when establishing a new connection
  - Now, with just a single WebSocket connection you can subscribe and unsubscribe to and from multiple streams
- Add support for limiting results by both `min_id` and `max_id` at the same time in REST API ([tateisu](https://www.okglobalcoinsg.com//pull/14776))
- Add `GET /api/v1/accounts/:id/featured_tags` to REST API ([noellabo](https://www.okglobalcoinsg.com//pull/11817), [noellabo](https://www.okglobalcoinsg.com//pull/15270))
- Add stoplight for object storage failures, return HTTP 503 in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/13043))
- Add optional `tootctl remove media` cronjob in Helm chart ([dunn](https://www.okglobalcoinsg.com//pull/14396))
- Add clean error message when `RAILS_ENV` is unset ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15381))

### Changed

- **Change media modals look in web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/15217), [Gargron](https://www.okglobalcoinsg.com//pull/15221), [Gargron](https://www.okglobalcoinsg.com//pull/15284), [Gargron](https://www.okglobalcoinsg.com//pull/15283), [Kjwon15](https://www.okglobalcoinsg.com//pull/15308), [noellabo](https://www.okglobalcoinsg.com//pull/15305), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15417))
  - Background of the overlay matches the color of the image
  - Action bar to interact with or open the toot from the modal
- Change order of announcements in admin UI to be newest-first ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15091))
- **Change account suspensions to be reversible by default** ([Gargron](https://www.okglobalcoinsg.com//pull/14726), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15152), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15106), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15100), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15099), [noellabo](https://www.okglobalcoinsg.com//pull/14855), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15380), [Gargron](https://www.okglobalcoinsg.com//pull/15420), [Gargron](https://www.okglobalcoinsg.com//pull/15414))
  - Suspensions no longer equal deletions
  - A suspended account can be unsuspended with minimal consequences for 30 days
  - Immediate deletion of data is still available as an explicit option
  - Suspended accounts can request an archive of their data through the UI
- Change REST API to return empty data for suspended accounts (14765)
- Change web UI to show empty profile for suspended accounts ([Gargron](https://www.okglobalcoinsg.com//pull/14766), [Gargron](https://www.okglobalcoinsg.com//pull/15345))
- Change featured hashtag suggestions to be recently used instead of most used ([abcang](https://www.okglobalcoinsg.com//pull/14760))
- Change direct toots to appear in the home feed again ([Gargron](https://www.okglobalcoinsg.com//pull/14711), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15182), [noellabo](https://www.okglobalcoinsg.com//pull/14727))
  - Return to treating all toots the same instead of trying to retrofit direct visibility into an instant messaging model
- Change email address validation to return more specific errors ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14565))
- Change HTTP signature requirements to include `Digest` header on `POST` requests ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15069))
- Change click area of video/audio player buttons to be bigger in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/15049))
- Change order of filters by alphabetic by "keyword or phrase" ([ariasuni](https://www.okglobalcoinsg.com//pull/15050))
- Change suspension of remote accounts to also undo outgoing follows ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15188))
- Change string "Home" to "Home and lists" in the filter creation screen ([ariasuni](https://www.okglobalcoinsg.com//pull/15139))
- Change string "Boost to original audience" to "Boost with original visibility" in web UI ([3n-k1](https://www.okglobalcoinsg.com//pull/14598))
- Change string "Show more" to "Show newer" and "Show older" on public pages ([ariasuni](https://www.okglobalcoinsg.com//pull/15052))
- Change order of announcements to be reverse chronological in web UI ([dariusk](https://www.okglobalcoinsg.com//pull/15065), [dariusk](https://www.okglobalcoinsg.com//pull/15070))
- Change RTL detection to rely on unicode-bidi paragraph by paragraph in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/14573))
- Change visibility icon next to timestamp to be clickable in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/15053), [mayaeh](https://www.okglobalcoinsg.com//pull/15055))
- Change public thread view to hide "Show thread" link ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15266))
- Change number format on about page from full to shortened ([Gargron](https://www.okglobalcoinsg.com//pull/15327))
- Change how scheduled tasks run in multi-process environments ([noellabo](https://www.okglobalcoinsg.com//pull/15314))
  - New dedicated queue `scheduler`
  - Runs by default when Sidekiq is executed with no options
  - Has to be added manually in a multi-process environment

### Removed

- Remove fade-in animation from modals in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/15199))
- Remove auto-redirect to direct messages in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/15142))
- Remove obsolete IndexedDB operations from web UI ([Gargron](https://www.okglobalcoinsg.com//pull/14730))
- Remove dependency on unused and unmaintained http_parser.rb gem ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14574))

### Fixed

- Fix layout on about page when contact account has a long username ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15357))
- Fix follow limit preventing re-following of a moved account ([Gargron](https://www.okglobalcoinsg.com//pull/14207), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15384))
- **Fix deletes not reaching every server that interacted with toot** ([Gargron](https://www.okglobalcoinsg.com//pull/15200))
  - Previously, delete of a toot would be primarily sent to the followers of its author, people mentioned in the toot, and people who reblogged the toot
  - Now, additionally, it is ensured that it is sent to people who replied to it, favourited it, and to the person it replies to even if that person is not mentioned
- Fix resolving an account through its non-canonical form (i.e. alternate domain) ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15187))
- Fix sending redundant ActivityPub events when processing remote account deletion ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15104))
- Fix Move handler not being triggered when failing to fetch target account ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15107))
- Fix downloading remote media files when server returns empty filename ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14867))
- Fix account processing failing because of large collections ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15027))
- Fix not being able to unfavorite toots one has lost access to ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15192))
- Fix not being able to unbookmark toots one has lost access to ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14604))
- Fix possible casing inconsistencies in hashtag search ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14906))
- Fix updating account counters when association is not yet created ([Gargron](https://www.okglobalcoinsg.com//pull/15108))
- Fix cookies not having a SameSite attribute ([Gargron](https://www.okglobalcoinsg.com//pull/15098))
- Fix poll ending notifications being created for each vote ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15071))
- Fix multiple boosts of a same toot erroneously appearing in TL ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14759))
- Fix asset builds not picking up `CDN_HOST` change ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14381))
- Fix desktop notifications permission prompt in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/14985), [Gargron](https://www.okglobalcoinsg.com//pull/15141), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13543), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15176))
  - Some time ago, browsers added a requirement that desktop notification prompts could only be displayed in response to a user-generated event (such as a click)
  - This means that for some time, users who haven't already given the permission before were not getting a prompt and as such were not receiving desktop notifications
- Fix "Mark media as sensitive" string not supporting pluralizations in other languages in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/15051))
- Fix glitched image uploads when canvas read access is blocked in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15180))
- Fix some account gallery items having empty labels in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15073))
- Fix alt-key hotkeys activating while typing in a text field in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14942))
- Fix wrong seek bar width on media player in web UI ([mfmfuyu](https://www.okglobalcoinsg.com//pull/15060))
- Fix logging out on mobile in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14901))
- Fix wrong click area for GIFVs in media modal in web UI ([noellabo](https://www.okglobalcoinsg.com//pull/14615))
- Fix unreadable placeholder text color in high contrast theme in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/14803))
- Fix scrolling issues when closing some dropdown menus in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14606))
- Fix notification filter bar incorrectly filtering gaps in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14808))
- Fix disabled boost icon being replaced by private boost icon on hover in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14456))
- Fix hashtag detection in compose form being different to server-side in web UI ([kedamaDQ](https://www.okglobalcoinsg.com//pull/14484), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14513))
- Fix home last read marker mishandling gaps in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14809))
- Fix unnecessary re-rendering of various components when typing in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/15286))
- Fix notifications being unnecessarily re-rendered in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15312))
- Fix column swiping animation logic in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15301))
- Fix inefficiency when fetching hashtag timeline ([noellabo](https://www.okglobalcoinsg.com//pull/14861), [akihikodaki](https://www.okglobalcoinsg.com//pull/14662))
- Fix inefficiency when fetching bookmarks ([akihikodaki](https://www.okglobalcoinsg.com//pull/14674))
- Fix inefficiency when fetching favourites ([akihikodaki](https://www.okglobalcoinsg.com//pull/14673))
- Fix inefficiency when fetching media-only account timeline ([akihikodaki](https://www.okglobalcoinsg.com//pull/14675))
- Fix inefficiency when deleting accounts ([Gargron](https://www.okglobalcoinsg.com//pull/15387), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15409), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15407), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15408), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15402), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/15416), [Gargron](https://www.okglobalcoinsg.com//pull/15421))
- Fix redundant query when processing batch actions on custom emojis ([niwatori24](https://www.okglobalcoinsg.com//pull/14534))
- Fix slow distinct queries where grouped queries are faster ([Gargron](https://www.okglobalcoinsg.com//pull/15287))
- Fix performance on instances list in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/15282))
- Fix server actor appearing in list of accounts in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14567))
- Fix "bootstrap timeline accounts" toggle in site settings in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15325))
- Fix PostgreSQL secret name for cronjob in Helm chart ([metal3d](https://www.okglobalcoinsg.com//pull/15072))
- Fix Procfile not being compatible with herokuish ([acuteaura](https://www.okglobalcoinsg.com//pull/12685))
- Fix installation of tini being split into multiple steps in Dockerfile ([ryncsn](https://www.okglobalcoinsg.com//pull/14686))

### Security

- Fix streaming API allowing connections to persist after access token invalidation ([Gargron](https://www.okglobalcoinsg.com//pull/15111))
- Fix 2FA/sign-in token sessions being valid after password change ([Gargron](https://www.okglobalcoinsg.com//pull/14802))
- Fix resolving accounts sometimes creating duplicate records for a given ActivityPub identifier ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15364))

## [3.2.2] - 2020-12-19
### Added

- Add `tootctl maintenance fix-duplicates` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14860), [Gargron](https://www.okglobalcoinsg.com//pull/15223))
  - Index corruption in the database?
  - This command is for you

### Removed

- Remove dependency on unused and unmaintained http_parser.rb gem ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14574))

### Fixed

- Fix Move handler not being triggered when failing to fetch target account ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15107))
- Fix downloading remote media files when server returns empty filename ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14867))
- Fix possible casing inconsistencies in hashtag search ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14906))
- Fix updating account counters when association is not yet created ([Gargron](https://www.okglobalcoinsg.com//pull/15108))
- Fix account processing failing because of large collections ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15027))
- Fix resolving an account through its non-canonical form (i.e. alternate domain) ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15187))
- Fix slow distinct queries where grouped queries are faster ([Gargron](https://www.okglobalcoinsg.com//pull/15287))

### Security

- Fix 2FA/sign-in token sessions being valid after password change ([Gargron](https://www.okglobalcoinsg.com//pull/14802))
- Fix resolving accounts sometimes creating duplicate records for a given ActivityPub identifier ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/15364))

## [3.2.1] - 2020-10-19
### Added

- Add support for latest HTTP Signatures spec draft ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14556))
- Add support for inlined objects in ActivityPub `to`/`cc` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14514))

### Changed

- Change actors to not be served at all without authentication in limited federation mode ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14800))
  - Previously, a bare version of an actor was served when not authenticated, i.e. username and public key
  - Because all actor fetch requests are signed using a separate system actor, that is no longer required

### Fixed

- Fix `tootctl media` commands not recognizing very large IDs ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14536))
- Fix crash when failing to load emoji picker in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14525))
- Fix contrast requirements in thumbnail color extraction ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14464))
- Fix audio/video player not using `CDN_HOST` on public pages ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14486))
- Fix private boost icon not being used on public pages ([OmmyZhang](https://www.okglobalcoinsg.com//pull/14471))
- Fix audio player on Safari in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14485), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14465))
- Fix dereferencing remote statuses not using the correct account for signature when receiving a targeted inbox delivery ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14656))
- Fix nil error in `tootctl media remove` ([noellabo](https://www.okglobalcoinsg.com//pull/14657))
- Fix videos with near-60 fps being rejected ([Gargron](https://www.okglobalcoinsg.com//pull/14684))
- Fix reported statuses not being included in warning e-mail ([Gargron](https://www.okglobalcoinsg.com//pull/14778))
- Fix `Reject` activities of `Follow` objects not correctly destroying a follow relationship ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14479))
- Fix inefficiencies in fan-out-on-write service ([Gargron](https://www.okglobalcoinsg.com//pull/14682), [noellabo](https://www.okglobalcoinsg.com//pull/14709))
- Fix timeout errors when trying to webfinger some IPv6 configurations ([Gargron](https://www.okglobalcoinsg.com//pull/14919))
- Fix files served as `application/octet-stream` being rejected without attempting mime type detection ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14452))

## [3.2.0] - 2020-07-27
### Added

- Add `SMTP_SSL` environment variable ([OmmyZhang](https://www.okglobalcoinsg.com//pull/14309))
- Add hotkey for toggling content warning input in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13987))
- **Add e-mail-based sign in challenge for users with disabled 2FA** ([Gargron](https://www.okglobalcoinsg.com//pull/14013))
  - If user tries signing in after:
    - Being inactive for a while
    - With a previously unknown IP
    - Without 2FA being enabled
  - Require to enter a token sent via e-mail before sigining in
- Add `limit` param to RSS feeds ([noellabo](https://www.okglobalcoinsg.com//pull/13743))
- Add `visibility` param to share page ([noellabo](https://www.okglobalcoinsg.com//pull/13023))
- Add blurhash to link previews ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13984), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14143), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13985), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/14267), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/14278), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14126), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14261), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14260))
  - In web UI, toots cannot be marked as sensitive unless there is media attached
  - However, it's possible to do via API or ActivityPub
  - Thumbnails of link previews of such posts now use blurhash in web UI
  - The Card entity in REST API has a new `blurhash` attribute
- Add support for `summary` field for media description in ActivityPub ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13763))
- Add hints about incomplete remote content to web UI ([Gargron](https://www.okglobalcoinsg.com//pull/14031), [noellabo](https://www.okglobalcoinsg.com//pull/14195))
- **Add personal notes for accounts** ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14148), [Gargron](https://www.okglobalcoinsg.com//pull/14208), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/14251))
  - To clarify, these are notes only you can see, to help you remember details
  - Notes can be viewed and edited from profiles in web UI
  - New REST API: `POST /api/v1/accounts/:id/note` with `comment` param
  - The Relationship entity in REST API has a new `note` attribute
- Add Helm chart ([dunn](https://www.okglobalcoinsg.com//pull/14090), [dunn](https://www.okglobalcoinsg.com//pull/14256), [dunn](https://www.okglobalcoinsg.com//pull/14245))
- **Add customizable thumbnails for audio and video attachments** ([Gargron](https://www.okglobalcoinsg.com//pull/14145), [Gargron](https://www.okglobalcoinsg.com//pull/14244), [Gargron](https://www.okglobalcoinsg.com//pull/14273), [Gargron](https://www.okglobalcoinsg.com//pull/14203), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14255), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14306), [noellabo](https://www.okglobalcoinsg.com//pull/14358), [noellabo](https://www.okglobalcoinsg.com//pull/14357))
  - Metadata (album, artist, etc) is no longer stripped from audio files
  - Album art is automatically extracted from audio files
  - Thumbnail can be manually uploaded for both audio and video attachments
  - Media upload APIs now support `thumbnail` param
    - On `POST /api/v1/media` and `POST /api/v2/media`
    - And on `PUT /api/v1/media/:id`
  - ActivityPub representation of media attachments represents custom thumbnails with an `icon` attribute
  - The Media Attachment entity in REST API now has a `preview_remote_url` to its `preview_url`, equivalent to `remote_url` to its `url`
- **Add color extraction for thumbnails** ([Gargron](https://www.okglobalcoinsg.com//pull/14209), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14264))
  - The `meta` attribute on the Media Attachment entity in REST API can now have a `colors` attribute which in turn contains three hex colors: `background`, `foreground`, and `accent`
  - The background color is chosen from the most dominant color around the edges of the thumbnail
  - The foreground and accent colors are chosen from the colors that are the most different from the background color using the CIEDE2000 algorithm
  - The most saturated color of the two is designated as the accent color
  - The one with the highest W3C contrast is designated as the foreground color
  - If there are not enough colors in the thumbnail, new ones are generated using a monochrome pattern
- Add a visibility indicator to toots in web UI ([noellabo](https://www.okglobalcoinsg.com//pull/14123), [highemerly](https://www.okglobalcoinsg.com//pull/14292))
- Add `tootctl email_domain_blocks` ([tateisu](https://www.okglobalcoinsg.com//pull/13589), [Gargron](https://www.okglobalcoinsg.com//pull/14147))
- Add "Add new domain block" to header of federation page in admin UI ([ariasuni](https://www.okglobalcoinsg.com//pull/13934))
- Add ability to keep emoji picker open with ctrl+click in web UI ([bclindner](https://www.okglobalcoinsg.com//pull/13896), [noellabo](https://www.okglobalcoinsg.com//pull/14096))
- Add custom icon for private boosts in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14380))
- Add support for Create and Update activities that don't inline objects in ActivityPub ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14359))
- Add support for Undo activities that don't inline activities in ActivityPub ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14346))

### Changed

- Change `.env.production.sample` to be leaner and cleaner ([Gargron](https://www.okglobalcoinsg.com//pull/14206))
  - It was overloaded as de-facto documentation and getting quite crowded
  - Defer to the actual documentation while still giving a minimal example
- Change `tootctl search deploy` to work faster and display progress ([Gargron](https://www.okglobalcoinsg.com//pull/14300))
- Change User-Agent of link preview fetching service to include "Bot" ([Gargron](https://www.okglobalcoinsg.com//pull/14248))
  - Some websites may not render OpenGraph tags into HTML if that's not the case
- Change behaviour to carry blocks over when someone migrates their followers ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14144))
- Change volume control and download buttons in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/14122))
- **Change design of audio players in web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/14095), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14281), [Gargron](https://www.okglobalcoinsg.com//pull/14282), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14118), [Gargron](https://www.okglobalcoinsg.com//pull/14199), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14338))
- Change reply filter to never filter own toots in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14128))
- Change boost button to no longer serve as visibility indicator in web UI ([noellabo](https://www.okglobalcoinsg.com//pull/14132), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14373))
- Change contrast of flash messages ([cchoi12](https://www.okglobalcoinsg.com//pull/13892))
- Change wording from "Hide media" to "Hide image/images" in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/13834))
- Change appearance of settings pages to be more consistent ([ariasuni](https://www.okglobalcoinsg.com//pull/13938))
- Change "Add media" tooltip to not include long list of formats in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/13954))
- Change how badly contrasting emoji are rendered in web UI ([leo60228](https://www.okglobalcoinsg.com//pull/13773), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13772), [mfmfuyu](https://www.okglobalcoinsg.com//pull/14020), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14015))
- Change structure of unavailable content section on about page ([ariasuni](https://www.okglobalcoinsg.com//pull/13930))
- Change behaviour to accept ActivityPub activities relayed through group actor ([noellabo](https://www.okglobalcoinsg.com//pull/14279))
- Change amount of processing retries for ActivityPub activities ([noellabo](https://www.okglobalcoinsg.com//pull/14355))

### Removed

- Remove the terms "blacklist" and "whitelist" from UX ([Gargron](https://www.okglobalcoinsg.com//pull/14149), [mayaeh](https://www.okglobalcoinsg.com//pull/14192))
  - Environment variables changed (old versions continue to work):
    - `WHITELIST_MODE` → `LIMITED_FEDERATION_MODE`
    - `EMAIL_DOMAIN_BLACKLIST` → `EMAIL_DOMAIN_DENYLIST`
    - `EMAIL_DOMAIN_WHITELIST` → `EMAIL_DOMAIN_ALLOWLIST`
  - CLI option changed:
    - `tootctl domains purge --whitelist-mode` → `tootctl domains purge --limited-federation-mode`
- Remove some unnecessary database indexes ([lfuelling](https://www.okglobalcoinsg.com//pull/13695), [noellabo](https://www.okglobalcoinsg.com//pull/14259))
- Remove unnecessary Node.js version upper bound ([ykzts](https://www.okglobalcoinsg.com//pull/14139))

### Fixed

- Fix `following` param not working when exact match is found in account search ([noellabo](https://www.okglobalcoinsg.com//pull/14394))
- Fix sometimes occurring duplicate mention notifications ([noellabo](https://www.okglobalcoinsg.com//pull/14378))
- Fix RSS feeds not being cacheable ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14368))
- Fix lack of locking around processing of Announce activities in ActivityPub ([noellabo](https://www.okglobalcoinsg.com//pull/14365))
- Fix boosted toots from blocked account not being retroactively removed from TL ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14339))
- Fix large shortened numbers (like 1.2K) using incorrect pluralization ([Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/14061))
- Fix streaming server trying to use empty password to connect to Redis when `REDIS_PASSWORD` is given but blank ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14135))
- Fix being unable to unboost posts when blocked by their author ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14308))
- Fix account domain block not properly unfollowing accounts from domain ([Gargron](https://www.okglobalcoinsg.com//pull/14304))
- Fix removing a domain allow wiping known accounts in open federation mode ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14298))
- Fix blocks and mutes pagination in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14275))
- Fix new posts pushing down origin of opened dropdown in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14271), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14348))
- Fix timeline markers not being saved sometimes ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13887), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13889), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/14155))
- Fix CSV uploads being rejected ([noellabo](https://www.okglobalcoinsg.com//pull/13835))
- Fix incompatibility with Elasticsearch 7.x ([noellabo](https://www.okglobalcoinsg.com//pull/13828))
- Fix being able to search posts where you're in the target audience but not actively mentioned ([noellabo](https://www.okglobalcoinsg.com//pull/13829))
- Fix non-local posts appearing on local-only hashtag timelines in web UI ([noellabo](https://www.okglobalcoinsg.com//pull/13827))
- Fix `tootctl media remove-orphans` choking on unknown files in storage ([Gargron](https://www.okglobalcoinsg.com//pull/13765))
- Fix `tootctl upgrade storage-schema` misbehaving ([Gargron](https://www.okglobalcoinsg.com//pull/13761), [angristan](https://www.okglobalcoinsg.com//pull/13768))
  - Fix it marking records as upgraded even though no files were moved
  - Fix it not working with S3 storage
  - Fix it not working with custom emojis
- Fix GIF reader raising incorrect exceptions ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13760))
- Fix hashtag search performing account search as well ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13758))
- Fix Webfinger returning wrong status code on malformed or missing param ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13759))
- Fix `rake mastodon:setup` error when some environment variables are set ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13928))
- Fix admin page crashing when trying to block an invalid domain name in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13884))
- Fix unsent toot confirmation dialog not popping up in single column mode in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13888))
- Fix performance of follow import ([noellabo](https://www.okglobalcoinsg.com//pull/13836))
  - Reduce timeout of Webfinger requests to that of other requests
  - Use circuit breakers to stop hitting unresponsive servers
  - Avoid hitting servers that are already known to be generally unavailable
- Fix filters ignoring media descriptions ([BenLubar](https://www.okglobalcoinsg.com//pull/13837))
- Fix some actions on custom emojis leading to cryptic errors in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13951))
- Fix ActivityPub serialization of replies when some of them are URIs ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13957))
- Fix `rake mastodon:setup` choking on environment variables containing `%` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13940))
- Fix account redirect confirmation message talking about moved followers ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13950))
- Fix avatars having the wrong size on public detailed status pages ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14140))
- Fix various issues around OpenGraph representation of media ([Gargron](https://www.okglobalcoinsg.com//pull/14133))
  - Pages containing audio no longer say "Attached: 1 image" in description
  - Audio attachments now represented as OpenGraph `og:audio`
  - The `twitter:player` page now uses Mastodon's proper audio/video player
  - Audio/video buffered bars now display correctly in audio/video player
  - Volume and progress bars now respond to movement/move smoother
- Fix audio/video/images/cards not reacting to window resizes in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/14130))
- Fix very wide media attachments resulting in too thin a thumbnail in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14127))
- Fix crash when merging posts into home feed after following someone ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14129))
- Fix unique username constraint for local users not being enforced in database ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14099))
- Fix unnecessary gap under video modal in web UI ([mfmfuyu](https://www.okglobalcoinsg.com//pull/14098))
- Fix 2FA and sign in token pages not respecting user locale ([mfmfuyu](https://www.okglobalcoinsg.com//pull/14087))
- Fix unapproved users being able to view profiles when in limited-federation mode *and* requiring approval for sign-ups ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14093))
- Fix initial audio volume not corresponding to what's displayed in audio player in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14057))
- Fix timelines sometimes jumping when closing modals in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14019))
- Fix memory usage of downloading remote files ([Gargron](https://www.okglobalcoinsg.com//pull/14184), [Gargron](https://www.okglobalcoinsg.com//pull/14181), [noellabo](https://www.okglobalcoinsg.com//pull/14356))
  - Don't read entire file (up to 40 MB) into memory
  - Read and write it to temp file in small chunks
- Fix inconsistent account header padding in web UI ([trwnh](https://www.okglobalcoinsg.com//pull/14179))
- Fix Thai being skipped from language detection ([Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/13989))
  - Since Thai has its own alphabet, it can be detected more reliably
- Fix broken hashtag column options styling in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14247))
- Fix pointer cursor being shown on toots that are not clickable in web UI ([arielrodrigues](https://www.okglobalcoinsg.com//pull/14185))
- Fix lock icon not being shown when locking account in profile settings ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14190))
- Fix domain blocks doing work the wrong way around ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13424))
  - Instead of suspending accounts one by one, mark all as suspended first (quick)
  - Only then proceed to start removing their data (slow)
  - Clear out media attachments in a separate worker (slow)

## [3.1.5] - 2020-07-07
### Security

- Fix media attachment enumeration ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/14254))
- Change rate limits for various paths ([Gargron](https://www.okglobalcoinsg.com//pull/14253))
- Fix other sessions not being logged out on password change ([Gargron](https://www.okglobalcoinsg.com//pull/14252))

## [3.1.4] - 2020-05-14
### Added

- Add `vi` to available locales ([taicv](https://www.okglobalcoinsg.com//pull/13542))
- Add ability to remove identity proofs from account ([Gargron](https://www.okglobalcoinsg.com//pull/13682))
- Add ability to exclude local content from federated timeline ([noellabo](https://www.okglobalcoinsg.com//pull/13504), [noellabo](https://www.okglobalcoinsg.com//pull/13745))
  - Add `remote` param to `GET /api/v1/timelines/public` REST API
  - Add `public/remote` / `public:remote` variants to streaming API
  - "Remote only" option in federated timeline column settings in web UI
- Add ability to exclude remote content from hashtag timelines in web UI ([noellabo](https://www.okglobalcoinsg.com//pull/13502))
  - No changes to REST API
  - "Local only" option in hashtag column settings in web UI
- Add Capistrano tasks that reload the services after deploying ([berkes](https://www.okglobalcoinsg.com//pull/12642))
- Add `invites_enabled` attribute to `GET /api/v1/instance` in REST API ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13501))
- Add `tootctl emoji export` command ([lfuelling](https://www.okglobalcoinsg.com//pull/13534))
- Add separate cache directory for non-local uploads ([Gargron](https://www.okglobalcoinsg.com//pull/12821), [Hanage999](https://www.okglobalcoinsg.com//pull/13593), [mayaeh](https://www.okglobalcoinsg.com//pull/13551))
  - Add `tootctl upgrade storage-schema` command to move old non-local uploads to the cache directory
- Add buttons to delete header and avatar from profile settings ([sternenseemann](https://www.okglobalcoinsg.com//pull/13234))
- Add emoji graphics and shortcodes from Twemoji 12.1.5 ([DeeUnderscore](https://www.okglobalcoinsg.com//pull/13021))

### Changed

- Change error message when trying to migrate to an account that does not have current account set as an alias to be more clear ([TheEvilSkeleton](https://www.okglobalcoinsg.com//pull/13746))
- Change delivery failure tracking to work with hostnames instead of URLs ([Gargron](https://www.okglobalcoinsg.com//pull/13437), [noellabo](https://www.okglobalcoinsg.com//pull/13481), [noellabo](https://www.okglobalcoinsg.com//pull/13482), [noellabo](https://www.okglobalcoinsg.com//pull/13535))
- Change Content-Security-Policy to not need unsafe-inline style-src ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13679), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13692), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13576), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13575), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13438))
- Change how RSS items are titled and formatted ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13592), [ykzts](https://www.okglobalcoinsg.com//pull/13591))

### Fixed

- Fix dropdown of muted and followed accounts offering option to hide boosts in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13748))
- Fix "You are already signed in" alert being shown at wrong times ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13547))
- Fix retrying of failed-to-download media files not actually working ([noellabo](https://www.okglobalcoinsg.com//pull/13741))
- Fix first poll option not being focused when adding a poll in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13740))
- Fix `sr` locale being selected over `sr-Latn` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13693))
- Fix error within error when limiting backtrace to 3 lines ([Gargron](https://www.okglobalcoinsg.com//pull/13120))
- Fix `tootctl media remove-orphans` crashing on "Import" files ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13685))
- Fix regression in `tootctl media remove-orphans` ([Gargron](https://www.okglobalcoinsg.com//pull/13405))
- Fix old unique jobs digests not having been cleaned up ([Gargron](https://www.okglobalcoinsg.com//pull/13683))
- Fix own following/followers not showing muted users ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13614))
- Fix list of followed people ignoring sorting on Follows & Followers page  ([taras2358](https://www.okglobalcoinsg.com//pull/13676))
- Fix wrong pgHero Content-Security-Policy when `CDN_HOST` is set ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13595))
- Fix needlessly deduplicating usernames on collisions with remote accounts when signing-up through SAML/CAS ([kaiyou](https://www.okglobalcoinsg.com//pull/13581))
- Fix page incorrectly scrolling when bringing up dropdown menus in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13574))
- Fix messed up z-index when NoScript blocks media/previews in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13449))
- Fix "See what's happening" page showing public instead of local timeline for logged-in users ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13499))
- Fix not being able to resolve public resources in development environment ([Gargron](https://www.okglobalcoinsg.com//pull/13505))
- Fix uninformative error message when uploading unsupported image files ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13540))
- Fix expanded video player issues in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13541), [eai04191](https://www.okglobalcoinsg.com//pull/13533))
- Fix and refactor keyboard navigation in dropdown menus in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13528))
- Fix uploaded image orientation being messed up in some browsers in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13493))
- Fix actions log crash when displaying updates of deleted announcements in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13489))
- Fix search not working due to proxy settings when using hidden services ([Gargron](https://www.okglobalcoinsg.com//pull/13488))
- Fix poll refresh button not being debounced in web UI ([rasjonell](https://www.okglobalcoinsg.com//pull/13485), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13490))
- Fix confusing error when failing to add an alias to an unknown account ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13480))
- Fix "Email changed" notification sometimes having wrong e-mail ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13475))
- Fix various issues on the account aliases page ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13452))
- Fix API footer link in web UI ([bubblineyuri](https://www.okglobalcoinsg.com//pull/13441))
- Fix pagination of following, followers, follow requests, blocks and mutes lists in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13445))
- Fix styling of polls in JS-less fallback on public pages ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13436))
- Fix trying to delete already deleted file when post-processing ([Gargron](https://www.okglobalcoinsg.com//pull/13406))

### Security

- Fix Doorkeeper vulnerability that exposed app secret to users who authorized the app and reset secret of the web UI that could have been exposed ([dependabot-preview[bot]](https://www.okglobalcoinsg.com//pull/13613), [Gargron](https://www.okglobalcoinsg.com//pull/13688))
  - For apps that self-register on behalf of every individual user (such as most mobile apps), this is a non-issue
  - The issue only affects developers of apps who are shared between multiple users, such as server-side apps like cross-posters

## [3.1.3] - 2020-04-05
### Added

- Add ability to filter audit log in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/13381))
- Add titles to warning presets in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/13252))
- Add option to include resolved DNS records when blacklisting e-mail domains in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/13254))
- Add ability to delete files uploaded for settings in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13192))
- Add sorting by username, creation and last activity in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13076))
- Add explanation as to why unlocked accounts may have follow requests in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13385))
- Add link to bookmarks to dropdown in web UI ([mayaeh](https://www.okglobalcoinsg.com//pull/13273))
- Add support for links to statuses in announcements to be opened in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13212), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13250))
- Add tooltips to audio/video player buttons in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/13203))
- Add submit button to the top of preferences pages ([guigeekz](https://www.okglobalcoinsg.com//pull/13068))
- Add specific rate limits for posting, following and reporting ([Gargron](https://www.okglobalcoinsg.com//pull/13172), [Gargron](https://www.okglobalcoinsg.com//pull/13390))
  - 300 posts every 3 hours
  - 400 follows or follow requests every 24 hours
  - 400 reports every 24 hours
- Add federation support for the "hide network" preference ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11673))
- Add `--skip-media-remove` option to `tootctl statuses remove` ([tateisu](https://www.okglobalcoinsg.com//pull/13080))

### Changed

- **Change design of polls in web UI** ([Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/13257), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13313))
- Change status click areas in web UI to be bigger ([ariasuni](https://www.okglobalcoinsg.com//pull/13327))
- **Change `tootctl media remove-orphans` to work for all classes** ([Gargron](https://www.okglobalcoinsg.com//pull/13316))
- **Change local media attachments to perform heavy processing asynchronously** ([Gargron](https://www.okglobalcoinsg.com//pull/13210))
- Change video uploads to always be converted to H264/MP4 ([Gargron](https://www.okglobalcoinsg.com//pull/13220), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13239), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13242))
- Change video uploads to enforce certain limits ([Gargron](https://www.okglobalcoinsg.com//pull/13218))
  - Dimensions smaller than 1920x1200px
  - Frame rate at most 60fps
- Change the tooltip "Toggle visibility" to "Hide media" in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/13199))
- Change description of privacy levels to be more intuitive in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/13197))
- Change GIF label to be displayed even when autoplay is enabled in web UI ([koyuawsmbrtn](https://www.okglobalcoinsg.com//pull/13209))
- Change the string "Hide everything from …" to "Block domain …" in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13178), [mayaeh](https://www.okglobalcoinsg.com//pull/13221))
- Change wording of media display preferences to be more intuitive ([ariasuni](https://www.okglobalcoinsg.com//pull/13198))

### Deprecated

- `POST /api/v1/media` → `POST /api/v2/media` ([Gargron](https://www.okglobalcoinsg.com//pull/13210))

### Fixed

- Fix `tootctl media remove-orphans` ignoring `PAPERCLIP_ROOT_PATH` ([Gargron](https://www.okglobalcoinsg.com//pull/13375))
- Fix returning results when searching for URL with non-zero offset ([Gargron](https://www.okglobalcoinsg.com//pull/13377))
- Fix pinning a column in web UI sometimes redirecting out of web UI ([Gargron](https://www.okglobalcoinsg.com//pull/13376))
- Fix background jobs not using locks like they are supposed to ([Gargron](https://www.okglobalcoinsg.com//pull/13361))
- Fix content warning being unnecessarily cleared when hiding content warning input in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13348))
- Fix "Show more" not switching to "Show less" on public pages ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13174))
- Fix import overwrite option not being selectable ([noellabo](https://www.okglobalcoinsg.com//pull/13347))
- Fix wrong color for ellipsis in boost confirmation dialog in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/13355))
- Fix unnecessary unfollowing when importing follows with overwrite option ([noellabo](https://www.okglobalcoinsg.com//pull/13350))
- Fix 404 and 410 API errors being silently discarded in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13279))
- Fix OCR not working on Safari because of unsupported worker-src CSP ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13323))
- Fix media not being marked sensitive when a content warning is set with no text ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13277))
- Fix crash after deleting announcements in web UI ([codesections](https://www.okglobalcoinsg.com//pull/13283), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/13312))
- Fix bookmarks not being searchable ([Kjwon15](https://www.okglobalcoinsg.com//pull/13271), [noellabo](https://www.okglobalcoinsg.com//pull/13293))
- Fix reported accounts not being whitelisted from further spam checks when resolving a spam check report ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13289))
- Fix web UI crash in single-column mode on prehistoric browsers ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13267))
- Fix some timeouts when searching for URLs ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13253))
- Fix detailed view of direct messages displaying a 0 boost count in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13244))
- Fix regression in “Edit media” modal in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13243))
- Fix public posts from silenced accounts not being changed to unlisted visibility ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13096))
- Fix error when searching for URLs that contain the mention syntax ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13151))
- Fix text area above/right of emoji picker being accidentally clickable in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/13148))
- Fix too large announcements not being scrollable in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13211))
- Fix `tootctl media remove-orphans` crashing when encountering invalid media ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13170))
- Fix installation failing when Redis password contains special characters ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13156))
- Fix announcements with fully-qualified mentions to local users crashing web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13164))

### Security

- Fix re-sending of e-mail confirmation not being rate limited ([Gargron](https://www.okglobalcoinsg.com//pull/13360))

## [v3.1.2] - 2020-02-27
### Added

- Add `--reset-password` option to `tootctl accounts modify` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13126))
- Add source-mapped stacktrace to error message in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13082))

### Fixed

- Fix dismissing an announcement twice raising an obscure error ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13124))
- Fix misleading error when attempting to re-send a pending follow request ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13133))
- Fix backups failing when files are missing from media attachments ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13146))
- Fix duplicate accounts being created when fetching an account for its key only ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13147))
- Fix `/web` redirecting to `/web/web` in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13128))
- Fix previously OStatus-based accounts not being detected as ActivityPub ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13129))
- Fix account JSON/RSS not being cacheable due to wrong mime type comparison ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13116))
- Fix old browsers crashing because of missing `finally` polyfill in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13115))
- Fix account's bio not being shown if there are no proofs/fields in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13075))
- Fix sign-ups without checked user agreement being accepted through the web form ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13088))
- Fix non-x64 architectures not being able to build Docker image because of hardcoded Node.js architecture ([SaraSmiseth](https://www.okglobalcoinsg.com//pull/13081))
- Fix invite request input not being shown on sign-up error if left empty ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13089))
- Fix some migration hints mentioning GitLab instead of Mastodon ([saper](https://www.okglobalcoinsg.com//pull/13084))

### Security

- Fix leak of arbitrary statuses through unfavourite action in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/13161))

## [3.1.1] - 2020-02-10
### Fixed

- Fix yanked dependency preventing installation ([mayaeh](https://www.okglobalcoinsg.com//pull/13059))

## [3.1.0] - 2020-02-09
### Added

- Add bookmarks ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/7107), [Gargron](https://www.okglobalcoinsg.com//pull/12494), [Gomasy](https://www.okglobalcoinsg.com//pull/12381))
- Add announcements ([Gargron](https://www.okglobalcoinsg.com//pull/12662), [Gargron](https://www.okglobalcoinsg.com//pull/12967), [Gargron](https://www.okglobalcoinsg.com//pull/12970), [Gargron](https://www.okglobalcoinsg.com//pull/12963), [Gargron](https://www.okglobalcoinsg.com//pull/12950), [Gargron](https://www.okglobalcoinsg.com//pull/12990), [Gargron](https://www.okglobalcoinsg.com//pull/12949), [Gargron](https://www.okglobalcoinsg.com//pull/12989), [Gargron](https://www.okglobalcoinsg.com//pull/12964), [Gargron](https://www.okglobalcoinsg.com//pull/12965), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12958), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12957), [Gargron](https://www.okglobalcoinsg.com//pull/12955), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12946), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12954))
- Add number animations in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/12948), [Gargron](https://www.okglobalcoinsg.com//pull/12971))
- Add `kab`, `is`, `kn`, `mr`, `ur` to available locales ([Gargron](https://www.okglobalcoinsg.com//pull/12882), [BoFFire](https://www.okglobalcoinsg.com//pull/12962), [Gargron](https://www.okglobalcoinsg.com//pull/12379))
- Add profile filter category ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12918))
- Add ability to add oneself to lists ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12271))
- Add hint how to contribute translations to preferences page ([Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12736))
- Add signatures to statuses in archive takeout ([noellabo](https://www.okglobalcoinsg.com//pull/12649))
- Add support for `magnet:` and `xmpp` links ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12905), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12709))
- Add `follow_request` notification type ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12198))
- Add ability to filter reports by account domain in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12154))
- Add link to search for users connected from the same IP address to admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12157))
- Add link to reports targeting a specific domain in admin view ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12513))
- Add support for EventSource streaming in web UI ([BenLubar](https://www.okglobalcoinsg.com//pull/12887))
- Add hotkey for opening media attachments in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12498), [Kjwon15](https://www.okglobalcoinsg.com//pull/12546))
- Add relationship-based options to status dropdowns in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/12377), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12535), [Gargron](https://www.okglobalcoinsg.com//pull/12430))
- Add support for submitting media description with `ctrl`+`enter` in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12272))
- Add download button to audio and video players in web UI ([NimaBoscarino](https://www.okglobalcoinsg.com//pull/12179))
- Add setting for whether to crop images in timelines in web UI ([duxovni](https://www.okglobalcoinsg.com//pull/12126))
- Add support for `Event` activities ([tcitworld](https://www.okglobalcoinsg.com//pull/12637))
- Add basic support for `Group` actors ([noellabo](https://www.okglobalcoinsg.com//pull/12071))
- Add `S3_OVERRIDE_PATH_STYLE` environment variable ([Gargron](https://www.okglobalcoinsg.com//pull/12594))
- Add `S3_OPEN_TIMEOUT` environment variable ([tateisu](https://www.okglobalcoinsg.com//pull/12459))
- Add `LDAP_MAIL` environment variable ([madmath03](https://www.okglobalcoinsg.com//pull/12053))
- Add `LDAP_UID_CONVERSION_ENABLED` environment variable ([madmath03](https://www.okglobalcoinsg.com//pull/12461))
- Add `--remote-only` option to `tootctl emoji purge` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12810))
- Add `tootctl media remove-orphans` ([Gargron](https://www.okglobalcoinsg.com//pull/12568), [Gargron](https://www.okglobalcoinsg.com//pull/12571))
- Add `tootctl media lookup` command ([irlcatgirl](https://www.okglobalcoinsg.com//pull/12283))
- Add cache for OEmbed endpoints to avoid extra HTTP requests ([Gargron](https://www.okglobalcoinsg.com//pull/12403))
- Add support for KaiOS arrow navigation to public pages ([nolanlawson](https://www.okglobalcoinsg.com//pull/12251))
- Add `discoverable` to accounts in REST API ([trwnh](https://www.okglobalcoinsg.com//pull/12508))
- Add admin setting to disable default follows ([ArisuOngaku](https://www.okglobalcoinsg.com//pull/12566))
- Add support for LDAP and PAM in the OAuth password grant strategy ([ntl-purism](https://www.okglobalcoinsg.com//pull/12390), [Gargron](https://www.okglobalcoinsg.com//pull/12743))
- Allow support for `Accept`/`Reject` activities with a non-embedded object ([puckipedia](https://www.okglobalcoinsg.com//pull/12199))
- Add "Show thread" button to public profiles ([Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/13000))

### Changed

- Change `last_status_at` to be a date, not datetime in REST API ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12966))
- Change followers page to relationships page in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/12927), [Gargron](https://www.okglobalcoinsg.com//pull/12934))
- Change reported media attachments to always be hidden in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/12879), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12907))
- Change string from "Disable" to "Disable login" in admin UI ([nileshkumar](https://www.okglobalcoinsg.com//pull/12201))
- Change report page structure in admin UI ([Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12615))
- Change swipe sensitivity to be lower on small screens in web UI ([umonaca](https://www.okglobalcoinsg.com//pull/12168))
- Change audio/video playback to stop playback when out of view in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/12486))
- Change media description label based on upload type in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12270))
- Change large numbers to render without decimal units in web UI ([noellabo](https://www.okglobalcoinsg.com//pull/12706))
- Change "Add a choice" button to be disabled rather than hidden when poll limit reached in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12319), [hinaloe](https://www.okglobalcoinsg.com//pull/12544))
- Change `tootctl statuses remove` to keep statuses favourited or bookmarked by local users ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11267), [Gomasy](https://www.okglobalcoinsg.com//pull/12818))
- Change domain block behavior to update user records (fast) before deleting data (slower) ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12247))
- Change behaviour to strip audio metadata on uploads ([hugogameiro](https://www.okglobalcoinsg.com//pull/12171))
- Change accepted length of remote media descriptions from 420 to 1,500 characters ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12262))
- Change preferences pages structure ([Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12497), [mayaeh](https://www.okglobalcoinsg.com//pull/12517), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12801), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12797), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12799), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12793))
- Change format of titles in RSS ([devkral](https://www.okglobalcoinsg.com//pull/8596))
- Change favourite icon animation from spring-based motion to CSS animation in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12175))
- Change minimum required Node.js version to 10, and default to 12 ([Shleeble](https://www.okglobalcoinsg.com//pull/12791), [mkody](https://www.okglobalcoinsg.com//pull/12906), [Shleeble](https://www.okglobalcoinsg.com//pull/12703))
- Change spam check to exempt server staff ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12874))
- Change to fallback to to `Create` audience when `object` has no defined audience ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12249))
- Change Twemoji library to 12.1.3 in web UI ([koyuawsmbrtn](https://www.okglobalcoinsg.com//pull/12342))
- Change blocked users to be hidden from following/followers lists ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12733))
- Change signature verification to ignore signatures with invalid host ([Gargron](https://www.okglobalcoinsg.com//pull/13033))

### Removed

- Remove unused dependencies ([ykzts](https://www.okglobalcoinsg.com//pull/12861), [mayaeh](https://www.okglobalcoinsg.com//pull/12826), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12822), [ykzts](https://www.okglobalcoinsg.com//pull/12533))

### Fixed

- Fix some translatable strings being used wrongly ([Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12569), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12589), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12502), [mayaeh](https://www.okglobalcoinsg.com//pull/12231))
- Fix headline of public timeline page when set to local-only ([ykzts](https://www.okglobalcoinsg.com//pull/12224))
- Fix space between tabs not being spread evenly in web UI ([Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12944), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12961), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12446))
- Fix interactive delays in database migrations with no TTY ([Gargron](https://www.okglobalcoinsg.com//pull/12969))
- Fix status overflowing in report dialog in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12959))
- Fix unlocalized dropdown button title in web UI ([Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/12947))
- Fix media attachments without file being uploadable ([Gargron](https://www.okglobalcoinsg.com//pull/12562))
- Fix unfollow confirmations in profile directory in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12922))
- Fix duplicate `description` meta tag on accounts public pages ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12923))
- Fix slow query of federated timeline ([notozeki](https://www.okglobalcoinsg.com//pull/12886))
- Fix not all of account's active IPs showing up in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/12909), [Gargron](https://www.okglobalcoinsg.com//pull/12943))
- Fix search by IP not using alternative browser sessions in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/12904))
- Fix “X new items” not showing up for slow mode on empty timelines in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12875))
- Fix OEmbed endpoint being inaccessible in secure mode ([Gargron](https://www.okglobalcoinsg.com//pull/12864))
- Fix proofs API being inaccessible in secure mode ([Gargron](https://www.okglobalcoinsg.com//pull/12495))
- Fix Ruby 2.7 incompatibilities ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12831), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12824), [Shleeble](https://www.okglobalcoinsg.com//pull/12759), [zunda](https://www.okglobalcoinsg.com//pull/12769))
- Fix invalid poll votes being accepted in REST API ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12601))
- Fix old migrations failing because of strong migrations update ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12787), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12692))
- Fix reuse of detailed status components in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12792))
- Fix base64-encoded file uploads not being possible in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/12748), [Gargron](https://www.okglobalcoinsg.com//pull/12857))
- Fix error due to missing authentication call in filters controller ([Gargron](https://www.okglobalcoinsg.com//pull/12746))
- Fix uncaught unknown format error in host meta controller ([Gargron](https://www.okglobalcoinsg.com//pull/12747))
- Fix URL search not returning private toots user has access to ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12742), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/12336))
- Fix cache digesting log noise on status embeds ([Gargron](https://www.okglobalcoinsg.com//pull/12750))
- Fix slowness due to layout thrashing when reloading a large set of statuses in web UI ([panarom](https://www.okglobalcoinsg.com//pull/12661), [panarom](https://www.okglobalcoinsg.com//pull/12744), [Gargron](https://www.okglobalcoinsg.com//pull/12712))
- Fix error when fetching followers/following from REST API when user has network hidden ([Gargron](https://www.okglobalcoinsg.com//pull/12716))
- Fix IDN mentions not being processed, IDN domains not being rendered ([Gargron](https://www.okglobalcoinsg.com//pull/12715), [Gargron](https://www.okglobalcoinsg.com//pull/13035), [Gargron](https://www.okglobalcoinsg.com//pull/13030))
- Fix error when searching for empty phrase ([Gargron](https://www.okglobalcoinsg.com//pull/12711))
- Fix backups stopping due to read timeouts ([chr-1x](https://www.okglobalcoinsg.com//pull/12281))
- Fix batch actions on non-pending tags in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12537))
- Fix sample `SAML_ACS_URL`, `SAML_ISSUER` ([orlea](https://www.okglobalcoinsg.com//pull/12669))
- Fix manual scrolling issue on Firefox/Windows in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12648))
- Fix archive takeout failing if total dump size exceeds 2GB ([scd31](https://www.okglobalcoinsg.com//pull/12602), [Gargron](https://www.okglobalcoinsg.com//pull/12653))
- Fix custom emoji category creation silently erroring out on duplicate category ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12647))
- Fix link crawler not specifying preferred content type ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12646))
- Fix featured hashtag setting page erroring out instead of rejecting invalid tags ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12436))
- Fix tooltip messages of single/multiple-choice polls switcher being reversed in web UI ([acid-chicken](https://www.okglobalcoinsg.com//pull/12616))
- Fix typo in help text of `tootctl statuses remove` ([trwnh](https://www.okglobalcoinsg.com//pull/12603))
- Fix generic HTTP 500 error on duplicate records ([Gargron](https://www.okglobalcoinsg.com//pull/12563))
- Fix old migration failing with new status default scope ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12493))
- Fix errors when using search API with no query ([Gargron](https://www.okglobalcoinsg.com//pull/12541), [trwnh](https://www.okglobalcoinsg.com//pull/12549))
- Fix poll options not being selectable via keyboard in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12538))
- Fix conversations not having an unread indicator in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/12506))
- Fix lost focus when modals open/close in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12437))
- Fix pending upload count not being decremented on error in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12499))
- Fix empty poll options not being removed on remote poll update ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12484))
- Fix OCR with delete & redraft in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12465))
- Fix blur behind closed registration message ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12442))
- Fix OEmbed discovery not handling different URL variants in query ([Gargron](https://www.okglobalcoinsg.com//pull/12439))
- Fix link crawler crashing on `<a>` tags without `href` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12159))
- Fix whitelisted subdomains being ignored in whitelist mode ([noiob](https://www.okglobalcoinsg.com//pull/12435))
- Fix broken audit log in whitelist mode in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12303))
- Fix unread indicator not honoring "Only media" option in local and federated timelines in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12330))
- Fix error when rebuilding home feeds ([dariusk](https://www.okglobalcoinsg.com//pull/12324))
- Fix relationship caches being broken as result of a follow request ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12299))
- Fix more items than the limit being uploadable in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12300))
- Fix various issues with account migration ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12301))
- Fix filtered out items being counted as pending items in slow mode in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12266))
- Fix notification filters not applying to poll options ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12269))
- Fix notification message for user's own poll saying it's a poll they voted on in web UI ([ykzts](https://www.okglobalcoinsg.com//pull/12219))
- Fix polls with an expiration not showing up as expired in web UI ([noellabo](https://www.okglobalcoinsg.com//pull/12222))
- Fix volume slider having an offset between cursor and slider in Chromium in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12158))
- Fix Vagrant image not accepting connections ([shrft](https://www.okglobalcoinsg.com//pull/12180))
- Fix batch actions being hidden on small screens in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12183))
- Fix incoming federation not working in whitelist mode ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12185))
- Fix error when passing empty `source` param to `PUT /api/v1/accounts/update_credentials` ([jglauche](https://www.okglobalcoinsg.com//pull/12259))
- Fix HTTP-based streaming API being cacheable by proxies ([BenLubar](https://www.okglobalcoinsg.com//pull/12945))
- Fix users being able to register while `tootctl self-destruct` is in progress ([Kjwon15](https://www.okglobalcoinsg.com//pull/12877))
- Fix microformats detection in link crawler not ignoring `h-card` links ([nightpool](https://www.okglobalcoinsg.com//pull/12189))
- Fix outline on full-screen video in web UI ([hinaloe](https://www.okglobalcoinsg.com//pull/12176))
- Fix TLD domain blocks not being editable ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12805))
- Fix Nanobox deploy hooks ([danhunsaker](https://www.okglobalcoinsg.com//pull/12663))
- Fix needlessly complicated SQL query when performing account search amongst followings ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12302))
- Fix favourites count not updating when unfavouriting in web UI ([NimaBoscarino](https://www.okglobalcoinsg.com//pull/12140))
- Fix occasional crash on scroll in Chromium in web UI ([hinaloe](https://www.okglobalcoinsg.com//pull/12274))
- Fix intersection observer not working in single-column mode web UI ([panarom](https://www.okglobalcoinsg.com//pull/12735))
- Fix voting issue with remote polls that contain trailing spaces ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12515))
- Fix dynamic elements not working in pgHero due to CSP rules ([ykzts](https://www.okglobalcoinsg.com//pull/12489))
- Fix overly verbose backtraces when delivering ActivityPub payloads ([zunda](https://www.okglobalcoinsg.com//pull/12798))
- Fix rendering `<a>` without `href` when scheme unsupported ([Gargron](https://www.okglobalcoinsg.com//pull/13040))
- Fix unfiltered params error when generating ActivityPub tag pagination ([Gargron](https://www.okglobalcoinsg.com//pull/13049))
- Fix malformed HTML causing uncaught error ([Gargron](https://www.okglobalcoinsg.com//pull/13042))
- Fix native share button not being displayed for unlisted toots ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/13045))
- Fix remote convertible media attachments (e.g. GIFs) not being saved ([Gargron](https://www.okglobalcoinsg.com//pull/13032))
- Fix account query not using faster index ([abcang](https://www.okglobalcoinsg.com//pull/13016))
- Fix error when sending moderation notification ([renatolond](https://www.okglobalcoinsg.com//pull/13014))

### Security

- Fix OEmbed leaking information about existence of non-public statuses ([Gargron](https://www.okglobalcoinsg.com//pull/12930))
- Fix password change/reset not immediately invalidating other sessions ([Gargron](https://www.okglobalcoinsg.com//pull/12928))
- Fix settings pages being cacheable by the browser ([Gargron](https://www.okglobalcoinsg.com//pull/12714))

## [3.0.1] - 2019-10-10
### Added

- Add `tootctl media usage` command ([Gargron](https://www.okglobalcoinsg.com//pull/12115))
- Add admin setting to auto-approve trending hashtags ([Gargron](https://www.okglobalcoinsg.com//pull/12122), [Gargron](https://www.okglobalcoinsg.com//pull/12130))

### Changed

- Change `tootctl media refresh` to skip already downloaded attachments ([Gargron](https://www.okglobalcoinsg.com//pull/12118))

### Removed

- Remove auto-silence behaviour from spam check ([Gargron](https://www.okglobalcoinsg.com//pull/12117))
- Remove HTML `lang` attribute from individual statuses in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/12124))
- Remove fallback to long description on sidebar and meta description ([Gargron](https://www.okglobalcoinsg.com//pull/12119))

### Fixed

- Fix preloaded JSON-LD context for identity not being used ([Gargron](https://www.okglobalcoinsg.com//pull/12138))
- Fix media editing modal changing dimensions once the image loads ([Gargron](https://www.okglobalcoinsg.com//pull/12131))
- Fix not showing whether a custom emoji has a local counterpart in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/12135))
- Fix attachment not being re-downloaded even if file is not stored ([Gargron](https://www.okglobalcoinsg.com//pull/12125))
- Fix old migration trying to use new column due to default status scope ([Gargron](https://www.okglobalcoinsg.com//pull/12095))
- Fix column back button missing for not found accounts ([trwnh](https://www.okglobalcoinsg.com//pull/12094))
- Fix issues with tootctl's parallelization and progress reporting ([Gargron](https://www.okglobalcoinsg.com//pull/12093), [Gargron](https://www.okglobalcoinsg.com//pull/12097))
- Fix existing user records with now-renamed `pt` locale ([Gargron](https://www.okglobalcoinsg.com//pull/12092))
- Fix hashtag timeline REST API accepting too many hashtags ([Gargron](https://www.okglobalcoinsg.com//pull/12091))
- Fix `GET /api/v1/instance` REST APIs being unavailable in secure mode ([Gargron](https://www.okglobalcoinsg.com//pull/12089))
- Fix performance of home feed regeneration and merging ([Gargron](https://www.okglobalcoinsg.com//pull/12084))
- Fix ffmpeg performance issues due to stdout buffer overflow ([hugogameiro](https://www.okglobalcoinsg.com//pull/12088))
- Fix S3 adapter retrying failing uploads with exponential backoff ([Gargron](https://www.okglobalcoinsg.com//pull/12085))
- Fix `tootctl accounts cull` advertising unused option flag ([Kjwon15](https://www.okglobalcoinsg.com//pull/12074))

## [3.0.0] - 2019-10-03
### Added

- Add "not available" label to unloaded media attachments in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/11715), [Gargron](https://www.okglobalcoinsg.com//pull/11745))
- **Add profile directory to web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/11688), [mayaeh](https://www.okglobalcoinsg.com//pull/11872))
  - Add profile directory opt-in federation
  - Add profile directory REST API
- Add special alert for throttled requests in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11677))
- Add confirmation modal when logging out from the web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11671))
- **Add audio player in web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/11644), [Gargron](https://www.okglobalcoinsg.com//pull/11652), [Gargron](https://www.okglobalcoinsg.com//pull/11654), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11629), [Gargron](https://www.okglobalcoinsg.com//pull/12056))
- **Add autosuggestions for hashtags in web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/11422), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11632), [Gargron](https://www.okglobalcoinsg.com//pull/11764), [Gargron](https://www.okglobalcoinsg.com//pull/11588), [Gargron](https://www.okglobalcoinsg.com//pull/11442))
- **Add media editing modal with OCR tool in web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/11563), [Gargron](https://www.okglobalcoinsg.com//pull/11566), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11575), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11576), [Gargron](https://www.okglobalcoinsg.com//pull/11577), [Gargron](https://www.okglobalcoinsg.com//pull/11573), [Gargron](https://www.okglobalcoinsg.com//pull/11571))
- Add indicator of unread notifications to window title when web UI is out of focus ([Gargron](https://www.okglobalcoinsg.com//pull/11560), [Gargron](https://www.okglobalcoinsg.com//pull/11572))
- Add indicator for which options you voted for in a poll in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11195))
- **Add search results pagination to web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/11409), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11447))
- **Add option to disable real-time updates in web UI ("slow mode")** ([Gargron](https://www.okglobalcoinsg.com//pull/9984), [ykzts](https://www.okglobalcoinsg.com//pull/11880), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11883), [Gargron](https://www.okglobalcoinsg.com//pull/11898), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11859))
- Add option to disable blurhash previews in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11188))
- Add native smooth scrolling when supported in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11207))
- Add scrolling to the search bar on focus in web UI ([Kjwon15](https://www.okglobalcoinsg.com//pull/12032))
- Add refresh button to list of rebloggers/favouriters in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/12031))
- Add error description and button to copy stack trace to web UI ([Gargron](https://www.okglobalcoinsg.com//pull/12033))
- Add search and sort functions to hashtag admin UI ([mayaeh](https://www.okglobalcoinsg.com//pull/11829), [Gargron](https://www.okglobalcoinsg.com//pull/11897), [mayaeh](https://www.okglobalcoinsg.com//pull/11875))
- Add setting for default search engine indexing in admin UI ([brortao](https://www.okglobalcoinsg.com//pull/11804))
- Add account bio to account view in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11473))
- **Add option to include reported statuses in warning e-mail from admin UI** ([Gargron](https://www.okglobalcoinsg.com//pull/11639), [Gargron](https://www.okglobalcoinsg.com//pull/11812), [Gargron](https://www.okglobalcoinsg.com//pull/11741), [Gargron](https://www.okglobalcoinsg.com//pull/11698), [mayaeh](https://www.okglobalcoinsg.com//pull/11765))
- Add number of pending accounts and pending hashtags to dashboard in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/11514))
- **Add account migration UI** ([Gargron](https://www.okglobalcoinsg.com//pull/11846), [noellabo](https://www.okglobalcoinsg.com//pull/11905), [noellabo](https://www.okglobalcoinsg.com//pull/11907), [noellabo](https://www.okglobalcoinsg.com//pull/11906), [noellabo](https://www.okglobalcoinsg.com//pull/11902))
- **Add table of contents to about page** ([Gargron](https://www.okglobalcoinsg.com//pull/11885), [ykzts](https://www.okglobalcoinsg.com//pull/11941), [ykzts](https://www.okglobalcoinsg.com//pull/11895), [Kjwon15](https://www.okglobalcoinsg.com//pull/11916))
- **Add password challenge to 2FA settings, e-mail notifications** ([Gargron](https://www.okglobalcoinsg.com//pull/11878))
- **Add optional public list of domain blocks with comments** ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11298), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11515), [Gargron](https://www.okglobalcoinsg.com//pull/11908))
- Add an RSS feed for featured hashtags ([noellabo](https://www.okglobalcoinsg.com//pull/10502))
- Add explanations to featured hashtags UI and profile ([Gargron](https://www.okglobalcoinsg.com//pull/11586))
- **Add hashtag trends with admin and user settings** ([Gargron](https://www.okglobalcoinsg.com//pull/11490), [Gargron](https://www.okglobalcoinsg.com//pull/11502), [Gargron](https://www.okglobalcoinsg.com//pull/11641), [Gargron](https://www.okglobalcoinsg.com//pull/11594), [Gargron](https://www.okglobalcoinsg.com//pull/11517), [mayaeh](https://www.okglobalcoinsg.com//pull/11845), [Gargron](https://www.okglobalcoinsg.com//pull/11774), [Gargron](https://www.okglobalcoinsg.com//pull/11712), [Gargron](https://www.okglobalcoinsg.com//pull/11791), [Gargron](https://www.okglobalcoinsg.com//pull/11743), [Gargron](https://www.okglobalcoinsg.com//pull/11740), [Gargron](https://www.okglobalcoinsg.com//pull/11714), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11631), [Sasha-Sorokin](https://www.okglobalcoinsg.com//pull/11569), [Gargron](https://www.okglobalcoinsg.com//pull/11524), [Gargron](https://www.okglobalcoinsg.com//pull/11513))
  - Add hashtag usage breakdown to admin UI
  - Add batch actions for hashtags to admin UI
  - Add trends to web UI
  - Add trends to public pages
  - Add user preference to hide trends
  - Add admin setting to disable trends
- **Add categories for custom emojis** ([Gargron](https://www.okglobalcoinsg.com//pull/11196), [Gargron](https://www.okglobalcoinsg.com//pull/11793), [Gargron](https://www.okglobalcoinsg.com//pull/11920), [highemerly](https://www.okglobalcoinsg.com//pull/11876))
  - Add custom emoji categories to emoji picker in web UI
  - Add `category` to custom emojis in REST API
  - Add batch actions for custom emojis in admin UI
- Add max image dimensions to error message ([raboof](https://www.okglobalcoinsg.com//pull/11552))
- Add aac, m4a, 3gp, amr, wma to allowed audio formats ([Gargron](https://www.okglobalcoinsg.com//pull/11342), [umonaca](https://www.okglobalcoinsg.com//pull/11687))
- **Add search syntax for operators and phrases** ([Gargron](https://www.okglobalcoinsg.com//pull/11411))
- **Add REST API for managing featured hashtags** ([noellabo](https://www.okglobalcoinsg.com//pull/11778))
- **Add REST API for managing timeline read markers** ([Gargron](https://www.okglobalcoinsg.com//pull/11762))
- Add `exclude_unreviewed` param to `GET /api/v2/search` REST API ([Gargron](https://www.okglobalcoinsg.com//pull/11977))
- Add `reason` param to `POST /api/v1/accounts` REST API ([Gargron](https://www.okglobalcoinsg.com//pull/12064))
- **Add ActivityPub secure mode** ([Gargron](https://www.okglobalcoinsg.com//pull/11269), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11332), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11295))
- Add HTTP signatures to all outgoing ActivityPub GET requests ([Gargron](https://www.okglobalcoinsg.com//pull/11284), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11300))
- Add support for ActivityPub Audio activities ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11189))
- Add ActivityPub actor representing the entire server ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11321), [rtucker](https://www.okglobalcoinsg.com//pull/11400), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11561), [Gargron](https://www.okglobalcoinsg.com//pull/11798))
- **Add whitelist mode** ([Gargron](https://www.okglobalcoinsg.com//pull/11291), [mayaeh](https://www.okglobalcoinsg.com//pull/11634))
- Add config of multipart threshold for S3 ([ykzts](https://www.okglobalcoinsg.com//pull/11924), [ykzts](https://www.okglobalcoinsg.com//pull/11944))
- Add health check endpoint for web ([ykzts](https://www.okglobalcoinsg.com//pull/11770), [ykzts](https://www.okglobalcoinsg.com//pull/11947))
- Add HTTP signature keyId to request log ([Gargron](https://www.okglobalcoinsg.com//pull/11591))
- Add `SMTP_REPLY_TO` environment variable ([hugogameiro](https://www.okglobalcoinsg.com//pull/11718))
- Add `tootctl preview_cards remove` command ([mayaeh](https://www.okglobalcoinsg.com//pull/11320))
- Add `tootctl media refresh` command ([Gargron](https://www.okglobalcoinsg.com//pull/11775))
- Add `tootctl cache recount` command ([Gargron](https://www.okglobalcoinsg.com//pull/11597))
- Add option to exclude suspended domains from `tootctl domains crawl` ([dariusk](https://www.okglobalcoinsg.com//pull/11454))
- Add parallelization to `tootctl search deploy` ([noellabo](https://www.okglobalcoinsg.com//pull/12051))
- Add soft delete for statuses for instant deletes through API ([Gargron](https://www.okglobalcoinsg.com//pull/11623), [Gargron](https://www.okglobalcoinsg.com//pull/11648))
- Add rails-level JSON caching ([Gargron](https://www.okglobalcoinsg.com//pull/11333), [Gargron](https://www.okglobalcoinsg.com//pull/11271))
- **Add request pool to improve delivery performance** ([Gargron](https://www.okglobalcoinsg.com//pull/10353), [ykzts](https://www.okglobalcoinsg.com//pull/11756))
- Add concurrent connection attempts to resolved IP addresses ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11757))
- Add index for remember_token to improve login performance ([abcang](https://www.okglobalcoinsg.com//pull/11881))
- **Add more accurate hashtag search** ([Gargron](https://www.okglobalcoinsg.com//pull/11579), [Gargron](https://www.okglobalcoinsg.com//pull/11427), [Gargron](https://www.okglobalcoinsg.com//pull/11448))
- **Add more accurate account search** ([Gargron](https://www.okglobalcoinsg.com//pull/11537), [Gargron](https://www.okglobalcoinsg.com//pull/11580))
- **Add a spam check** ([Gargron](https://www.okglobalcoinsg.com//pull/11217), [Gargron](https://www.okglobalcoinsg.com//pull/11806), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11296))
- Add new languages ([Gargron](https://www.okglobalcoinsg.com//pull/12062))
  - Breton
  - Spanish (Argentina)
  - Estonian
  - Macedonian
  - New Norwegian
- Add NodeInfo endpoint ([Gargron](https://www.okglobalcoinsg.com//pull/12002), [Gargron](https://www.okglobalcoinsg.com//pull/12058))

### Changed

- **Change conversations UI** ([Gargron](https://www.okglobalcoinsg.com//pull/11896))
- Change dashboard to short number notation ([noellabo](https://www.okglobalcoinsg.com//pull/11847), [noellabo](https://www.okglobalcoinsg.com//pull/11911))
- Change REST API `GET /api/v1/timelines/public` to require authentication when public preview is off ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11802))
- Change REST API `POST /api/v1/follow_requests/:id/(approve|reject)` to return relationship ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11800))
- Change rate limit for media proxy ([ykzts](https://www.okglobalcoinsg.com//pull/11814))
- Change unlisted custom emoji to not appear in autosuggestions ([Gargron](https://www.okglobalcoinsg.com//pull/11818))
- Change max length of media descriptions from 420 to 1500 characters ([Gargron](https://www.okglobalcoinsg.com//pull/11819), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11836))
- **Change deletes to preserve soft-deleted statuses in unresolved reports** ([Gargron](https://www.okglobalcoinsg.com//pull/11805))
- **Change tootctl to use inline parallelization instead of Sidekiq** ([Gargron](https://www.okglobalcoinsg.com//pull/11776))
- **Change account deletion page to have better explanations** ([Gargron](https://www.okglobalcoinsg.com//pull/11753), [Gargron](https://www.okglobalcoinsg.com//pull/11763))
- Change hashtag component in web UI to show numbers for 2 last days ([Gargron](https://www.okglobalcoinsg.com//pull/11742), [Gargron](https://www.okglobalcoinsg.com//pull/11755), [Gargron](https://www.okglobalcoinsg.com//pull/11754))
- Change OpenGraph description on sign-up page to reflect invite ([Gargron](https://www.okglobalcoinsg.com//pull/11744))
- Change layout of public profile directory to be the same as in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/11705))
- Change detailed status child ordering to sort self-replies on top ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11686))
- Change window resize handler to switch to/from mobile layout as soon as needed ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11656))
- Change icon button styles to make hover/focus states more obvious ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11474))
- Change contrast of status links that are not mentions or hashtags ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11406))
- **Change hashtags to preserve first-used casing** ([Gargron](https://www.okglobalcoinsg.com//pull/11416), [Gargron](https://www.okglobalcoinsg.com//pull/11508), [Gargron](https://www.okglobalcoinsg.com//pull/11504), [Gargron](https://www.okglobalcoinsg.com//pull/11507), [Gargron](https://www.okglobalcoinsg.com//pull/11441))
- **Change unconfirmed user login behaviour** ([Gargron](https://www.okglobalcoinsg.com//pull/11375), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11394), [Gargron](https://www.okglobalcoinsg.com//pull/11860))
- **Change single-column mode to scroll the whole page** ([Gargron](https://www.okglobalcoinsg.com//pull/11359), [Gargron](https://www.okglobalcoinsg.com//pull/11894), [Gargron](https://www.okglobalcoinsg.com//pull/11891), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11655), [Gargron](https://www.okglobalcoinsg.com//pull/11463), [Gargron](https://www.okglobalcoinsg.com//pull/11458), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11395), [Gargron](https://www.okglobalcoinsg.com//pull/11418))
- Change `tootctl accounts follow` to only work with local accounts ([angristan](https://www.okglobalcoinsg.com//pull/11592))
- Change Dockerfile ([Shleeble](https://www.okglobalcoinsg.com//pull/11710), [ykzts](https://www.okglobalcoinsg.com//pull/11768), [Shleeble](https://www.okglobalcoinsg.com//pull/11707))
- Change supported Node versions to include v12 ([abcang](https://www.okglobalcoinsg.com//pull/11706))
- Change Portuguese language from `pt` to `pt-PT` ([Gargron](https://www.okglobalcoinsg.com//pull/11820))
- Change domain block silence to always require approval on follow ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11975))
- Change link preview fetcher to not perform a HEAD request first ([Gargron](https://www.okglobalcoinsg.com//pull/12028))
- Change `tootctl domains purge` to accept multiple domains at once ([Gargron](https://www.okglobalcoinsg.com//pull/12046))

### Removed

- **Remove OStatus support** ([Gargron](https://www.okglobalcoinsg.com//pull/11205), [Gargron](https://www.okglobalcoinsg.com//pull/11303), [Gargron](https://www.okglobalcoinsg.com//pull/11460), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11280), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11278))
- Remove Atom feeds and old URLs in the form of `GET /:username/updates/:id` ([Gargron](https://www.okglobalcoinsg.com//pull/11247))
- Remove WebP support ([angristan](https://www.okglobalcoinsg.com//pull/11589))
- Remove deprecated config options from Heroku and Scalingo ([ykzts](https://www.okglobalcoinsg.com//pull/11925))
- Remove deprecated REST API `GET /api/v1/search` API ([Gargron](https://www.okglobalcoinsg.com//pull/11823))
- Remove deprecated REST API `GET /api/v1/statuses/:id/card` ([Gargron](https://www.okglobalcoinsg.com//pull/11213))
- Remove deprecated REST API `POST /api/v1/notifications/dismiss?id=:id` ([Gargron](https://www.okglobalcoinsg.com//pull/11214))
- Remove deprecated REST API `GET /api/v1/timelines/direct` ([Gargron](https://www.okglobalcoinsg.com//pull/11212))

### Fixed

- Fix manifest warning ([ykzts](https://www.okglobalcoinsg.com//pull/11767))
- Fix admin UI for custom emoji not respecting GIF autoplay preference ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11801))
- Fix page body not being scrollable in admin/settings layout ([Gargron](https://www.okglobalcoinsg.com//pull/11893))
- Fix placeholder colors for inputs not being explicitly defined ([Gargron](https://www.okglobalcoinsg.com//pull/11890))
- Fix incorrect enclosure length in RSS ([tsia](https://www.okglobalcoinsg.com//pull/11889))
- Fix TOTP codes not being filtered from logs during enabling/disabling ([Gargron](https://www.okglobalcoinsg.com//pull/11877))
- Fix webfinger response not returning 410 when account is suspended ([Gargron](https://www.okglobalcoinsg.com//pull/11869))
- Fix ActivityPub Move handler queuing jobs that will fail if account is suspended ([Gargron](https://www.okglobalcoinsg.com//pull/11864))
- Fix SSO login not using existing account when e-mail is verified ([Gargron](https://www.okglobalcoinsg.com//pull/11862))
- Fix web UI allowing uploads past status limit via drag & drop ([Gargron](https://www.okglobalcoinsg.com//pull/11863))
- Fix expiring polls not being displayed as such in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11835))
- Fix 2FA challenge and password challenge for non-database users ([Gargron](https://www.okglobalcoinsg.com//pull/11831), [Gargron](https://www.okglobalcoinsg.com//pull/11943))
- Fix profile fields overflowing page width in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/11828))
- Fix web push subscriptions being deleted on rate limit or timeout ([Gargron](https://www.okglobalcoinsg.com//pull/11826))
- Fix display of long poll options in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11717), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11833))
- Fix search API not resolving URL when `type` is given ([Gargron](https://www.okglobalcoinsg.com//pull/11822))
- Fix hashtags being split by ZWNJ character ([Gargron](https://www.okglobalcoinsg.com//pull/11821))
- Fix scroll position resetting when opening media modals in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/11815))
- Fix duplicate HTML IDs on about page ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11803))
- Fix admin UI showing superfluous reject media/reports on suspended domain blocks ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11749))
- Fix ActivityPub context not being dynamically computed ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11746))
- Fix Mastodon logo style on hover on public pages' footer ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11735))
- Fix height of dashboard counters ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11736))
- Fix custom emoji animation on hover in web UI directory bios ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11716))
- Fix non-numbers being passed to Redis and causing an error ([Gargron](https://www.okglobalcoinsg.com//pull/11697))
- Fix error in REST API for an account's statuses ([Gargron](https://www.okglobalcoinsg.com//pull/11700))
- Fix uncaught error when resource param is missing in Webfinger request ([Gargron](https://www.okglobalcoinsg.com//pull/11701))
- Fix uncaught domain normalization error in remote follow ([Gargron](https://www.okglobalcoinsg.com//pull/11703))
- Fix uncaught 422 and 500 errors ([Gargron](https://www.okglobalcoinsg.com//pull/11590), [Gargron](https://www.okglobalcoinsg.com//pull/11811))
- Fix uncaught parameter missing exceptions and missing error templates ([Gargron](https://www.okglobalcoinsg.com//pull/11702))
- Fix encoding error when checking e-mail MX records ([Gargron](https://www.okglobalcoinsg.com//pull/11696))
- Fix items in StatusContent render list not all having a key ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11645))
- Fix remote and staff-removed statuses leaving media behind for a day ([Gargron](https://www.okglobalcoinsg.com//pull/11638))
- Fix CSP needlessly allowing blob URLs in script-src ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11620))
- Fix ignoring whole status because of one invalid hashtag ([Gargron](https://www.okglobalcoinsg.com//pull/11621))
- Fix hidden statuses losing focus ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11208))
- Fix loading bar being obscured by other elements in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/11598))
- Fix multiple issues with replies collection for pages further than self-replies ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11582))
- Fix blurhash and autoplay not working on public pages ([Gargron](https://www.okglobalcoinsg.com//pull/11585))
- Fix 422 being returned instead of 404 when POSTing to unmatched routes ([Gargron](https://www.okglobalcoinsg.com//pull/11574), [Gargron](https://www.okglobalcoinsg.com//pull/11704))
- Fix client-side resizing of image uploads ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11570))
- Fix short number formatting for numbers above million in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/11559))
- Fix ActivityPub and REST API queries setting cookies and preventing caching ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11539), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11557), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11336), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11331))
- Fix some emojis in profile metadata labels are not emojified. ([kedamaDQ](https://www.okglobalcoinsg.com//pull/11534))
- Fix account search always returning exact match on paginated results ([Gargron](https://www.okglobalcoinsg.com//pull/11525))
- Fix acct URIs with IDN domains not being resolved ([Gargron](https://www.okglobalcoinsg.com//pull/11520))
- Fix admin dashboard missing latest features ([Gargron](https://www.okglobalcoinsg.com//pull/11505))
- Fix jumping of toot date when clicking spoiler button ([ariasuni](https://www.okglobalcoinsg.com//pull/11449))
- Fix boost to original audience not working on mobile in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11371))
- Fix handling of webfinger redirects in ResolveAccountService ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11279))
- Fix URLs appearing twice in errors of ActivityPub::DeliveryWorker ([Gargron](https://www.okglobalcoinsg.com//pull/11231))
- Fix support for HTTP proxies ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11245))
- Fix HTTP requests to IPv6 hosts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11240))
- Fix error in Elasticsearch index import ([mayaeh](https://www.okglobalcoinsg.com//pull/11192))
- Fix duplicate account error when seeding development database ([ysksn](https://www.okglobalcoinsg.com//pull/11366))
- Fix performance of session clean-up scheduler ([abcang](https://www.okglobalcoinsg.com//pull/11871))
- Fix older migrations not running ([zunda](https://www.okglobalcoinsg.com//pull/11377))
- Fix URLs counting towards RTL detection ([ahangarha](https://www.okglobalcoinsg.com//pull/11759))
- Fix unnecessary status re-rendering in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11211))
- Fix http_parser.rb gem not being compiled when no network available ([petabyteboy](https://www.okglobalcoinsg.com//pull/11444))
- Fix muted text color not applying to all text ([trwnh](https://www.okglobalcoinsg.com//pull/11996))
- Fix follower/following lists resetting on back-navigation in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/11986))
- Fix n+1 query when approving multiple follow requests ([abcang](https://www.okglobalcoinsg.com//pull/12004))
- Fix records not being indexed into Elasticsearch sometimes ([Gargron](https://www.okglobalcoinsg.com//pull/12024))
- Fix needlessly indexing unsearchable statuses into Elasticsearch ([Gargron](https://www.okglobalcoinsg.com//pull/12041))
- Fix new user bootstrapping crashing when to-be-followed accounts are invalid ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/12037))
- Fix featured hashtag URL being interpreted as media or replies tab ([Gargron](https://www.okglobalcoinsg.com//pull/12048))
- Fix account counters being overwritten by parallel writes ([Gargron](https://www.okglobalcoinsg.com//pull/12045))

### Security

- Fix performance of GIF re-encoding and always strip EXIF data from videos ([Gargron](https://www.okglobalcoinsg.com//pull/12057))

## [2.9.3] - 2019-08-10
### Added

- Add GIF and WebP support for custom emojis ([Gargron](https://www.okglobalcoinsg.com//pull/11519))
- Add logout link to dropdown menu in web UI ([koyuawsmbrtn](https://www.okglobalcoinsg.com//pull/11353))
- Add indication that text search is unavailable in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11112), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11202))
- Add `suffix` to `Mastodon::Version` to help forks ([clarfon](https://www.okglobalcoinsg.com//pull/11407))
- Add on-hover animation to animated custom emoji in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11348), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11404), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11522))
- Add custom emoji support in profile metadata labels ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11350))

### Changed

- Change default interface of web and streaming from 0.0.0.0 to 127.0.0.1 ([Gargron](https://www.okglobalcoinsg.com//pull/11302), [zunda](https://www.okglobalcoinsg.com//pull/11378), [Gargron](https://www.okglobalcoinsg.com//pull/11351), [zunda](https://www.okglobalcoinsg.com//pull/11326))
- Change the retry limit of web push notifications ([highemerly](https://www.okglobalcoinsg.com//pull/11292))
- Change ActivityPub deliveries to not retry HTTP 501 errors ([Gargron](https://www.okglobalcoinsg.com//pull/11233))
- Change language detection to include hashtags as words ([Gargron](https://www.okglobalcoinsg.com//pull/11341))
- Change terms and privacy policy pages to always be accessible ([Gargron](https://www.okglobalcoinsg.com//pull/11334))
- Change robots tag to include `noarchive` when user opts out of indexing ([Kjwon15](https://www.okglobalcoinsg.com//pull/11421))

### Fixed

- Fix account domain block not clearing out notifications ([Gargron](https://www.okglobalcoinsg.com//pull/11393))
- Fix incorrect locale sometimes being detected for browser ([Gargron](https://www.okglobalcoinsg.com//pull/8657))
- Fix crash when saving invalid domain name ([Gargron](https://www.okglobalcoinsg.com//pull/11528))
- Fix pinned statuses REST API returning pagination headers ([Gargron](https://www.okglobalcoinsg.com//pull/11526))
- Fix "cancel follow request" button having unreadable text in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/11521))
- Fix image uploads being blank when canvas read access is blocked ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11499))
- Fix avatars not being animated on hover when not logged in ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11349))
- Fix overzealous sanitization of HTML lists ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11354))
- Fix block crashing when a follow request exists ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11288))
- Fix backup service crashing when an attachment is missing ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11241))
- Fix account moderation action always sending e-mail notification ([Gargron](https://www.okglobalcoinsg.com//pull/11242))
- Fix swiping columns on mobile sometimes failing in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11200))
- Fix wrong actor URI being serialized into poll updates ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11194))
- Fix statsd UDP sockets not being cleaned up in Sidekiq ([Gargron](https://www.okglobalcoinsg.com//pull/11230))
- Fix expiration date of filters being set to "never" when editing them ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11204))
- Fix support for MP4 files that are actually M4V files ([Gargron](https://www.okglobalcoinsg.com//pull/11210))
- Fix `alerts` not being typecast correctly in push subscription in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/11343))
- Fix some notices staying on unrelated pages ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11364))
- Fix unboosting sometimes preventing a boost from reappearing on feed ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11405), [Gargron](https://www.okglobalcoinsg.com//pull/11450))
- Fix only one middle dot being recognized in hashtags ([Gargron](https://www.okglobalcoinsg.com//pull/11345), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11363))
- Fix unnecessary SQL query performed on unauthenticated requests ([Gargron](https://www.okglobalcoinsg.com//pull/11179))
- Fix incorrect timestamp displayed on featured tags ([Kjwon15](https://www.okglobalcoinsg.com//pull/11477))
- Fix privacy dropdown active state when dropdown is placed on top of it ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11495))
- Fix filters not being applied to poll options ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11174))
- Fix keyboard navigation on various dropdowns ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11511), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11492), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11491))
- Fix keyboard navigation in modals ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11493))
- Fix image conversation being non-deterministic due to timestamps ([Gargron](https://www.okglobalcoinsg.com//pull/11408))
- Fix web UI performance ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11211), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11234))
- Fix scrolling to compose form when not necessary in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11246), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/11182))
- Fix save button being enabled when list title is empty in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11475))
- Fix poll expiration not being pre-filled on delete & redraft in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11203))
- Fix content warning sometimes being set when not requested in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11206))

### Security

- Fix invites not being disabled upon account suspension ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11412))
- Fix blocked domains still being able to fill database with account records ([Gargron](https://www.okglobalcoinsg.com//pull/11219))

## [2.9.2] - 2019-06-22
### Added

- Add `short_description` and `approval_required` to `GET /api/v1/instance` ([Gargron](https://www.okglobalcoinsg.com//pull/11146))

### Changed

- Change camera icon to paperclip icon in upload form ([koyuawsmbrtn](https://www.okglobalcoinsg.com//pull/11149))

### Fixed

- Fix audio-only OGG and WebM files not being processed as such ([Gargron](https://www.okglobalcoinsg.com//pull/11151))
- Fix audio not being downloaded from remote servers ([Gargron](https://www.okglobalcoinsg.com//pull/11145))

## [2.9.1] - 2019-06-22
### Added

- Add moderation API ([Gargron](https://www.okglobalcoinsg.com//pull/9387))
- Add audio uploads ([Gargron](https://www.okglobalcoinsg.com//pull/11123), [Gargron](https://www.okglobalcoinsg.com//pull/11141))

### Changed

- Change domain blocks to automatically support subdomains ([Gargron](https://www.okglobalcoinsg.com//pull/11138))
- Change Nanobox configuration to bring it up to date ([danhunsaker](https://www.okglobalcoinsg.com//pull/11083))

### Removed

- Remove expensive counters from federation page in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/11139))

### Fixed

- Fix converted media being saved with original extension and mime type ([Gargron](https://www.okglobalcoinsg.com//pull/11130))
- Fix layout of identity proofs settings ([acid-chicken](https://www.okglobalcoinsg.com//pull/11126))
- Fix active scope only returning suspended users ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11111))
- Fix sanitizer making block level elements unreadable ([Gargron](https://www.okglobalcoinsg.com//pull/10836))
- Fix label for site theme not being translated in admin UI ([palindromordnilap](https://www.okglobalcoinsg.com//pull/11121))
- Fix statuses not being filtered irreversibly in web UI under some circumstances ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11113))
- Fix scrolling behaviour in compose form ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11093))

## [2.9.0] - 2019-06-13
### Added

- **Add single-column mode in web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/10807), [Gargron](https://www.okglobalcoinsg.com//pull/10848), [Gargron](https://www.okglobalcoinsg.com//pull/11003), [Gargron](https://www.okglobalcoinsg.com//pull/10961), [Hanage999](https://www.okglobalcoinsg.com//pull/10915), [noellabo](https://www.okglobalcoinsg.com//pull/10917), [abcang](https://www.okglobalcoinsg.com//pull/10859), [Gargron](https://www.okglobalcoinsg.com//pull/10820), [Gargron](https://www.okglobalcoinsg.com//pull/10835), [Gargron](https://www.okglobalcoinsg.com//pull/10809), [Gargron](https://www.okglobalcoinsg.com//pull/10963), [noellabo](https://www.okglobalcoinsg.com//pull/10883), [Hanage999](https://www.okglobalcoinsg.com//pull/10839))
- Add waiting time to the list of pending accounts in admin UI ([Gargron](https://www.okglobalcoinsg.com//pull/10985))
- Add a keyboard shortcut to hide/show media in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10647), [Gargron](https://www.okglobalcoinsg.com//pull/10838), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10872))
- Add `account_id` param to `GET /api/v1/notifications` ([pwoolcoc](https://www.okglobalcoinsg.com//pull/10796))
- Add confirmation modal for unboosting toots in web UI ([aurelien-reeves](https://www.okglobalcoinsg.com//pull/10287))
- Add emoji suggestions to content warning and poll option fields in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10555))
- Add `source` attribute to response of `DELETE /api/v1/statuses/:id` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10669))
- Add some caching for HTML versions of public status pages ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10701))
- Add button to conveniently copy OAuth code ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/11065))

### Changed

- **Change default layout to single column in web UI** ([Gargron](https://www.okglobalcoinsg.com//pull/10847))
- **Change light theme** ([Gargron](https://www.okglobalcoinsg.com//pull/10992), [Gargron](https://www.okglobalcoinsg.com//pull/10996), [yuzulabo](https://www.okglobalcoinsg.com//pull/10754), [Gargron](https://www.okglobalcoinsg.com//pull/10845))
- **Change preferences page into appearance, notifications, and other** ([Gargron](https://www.okglobalcoinsg.com//pull/10977), [Gargron](https://www.okglobalcoinsg.com//pull/10988))
- Change priority of delete activity forwards for replies and reblogs ([Gargron](https://www.okglobalcoinsg.com//pull/11002))
- Change Mastodon logo to use primary text color of the given theme ([Gargron](https://www.okglobalcoinsg.com//pull/10994))
- Change reblogs counter to be updated when boosted privately ([Gargron](https://www.okglobalcoinsg.com//pull/10964))
- Change bio limit from 160 to 500 characters ([trwnh](https://www.okglobalcoinsg.com//pull/10790))
- Change API rate limiting to reduce allowed unauthenticated requests ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10860), [hinaloe](https://www.okglobalcoinsg.com//pull/10868), [mayaeh](https://www.okglobalcoinsg.com//pull/10867))
- Change help text of `tootctl emoji import` command to specify a gzipped TAR archive is required ([dariusk](https://www.okglobalcoinsg.com//pull/11000))
- Change web UI to hide poll options behind content warnings ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10983))
- Change silencing to ensure local effects and remote effects are the same for silenced local users ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10575))
- Change `tootctl domains purge` to remove custom emoji as well ([Kjwon15](https://www.okglobalcoinsg.com//pull/10721))
- Change Docker image to keep `apt` working ([SuperSandro2000](https://www.okglobalcoinsg.com//pull/10830))

### Removed

- Remove `dist-upgrade` from Docker image ([SuperSandro2000](https://www.okglobalcoinsg.com//pull/10822))

### Fixed

- Fix RTL layout not being RTL within the columns area in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10990))
- Fix display of alternative text when a media attachment is not available in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10981))
- Fix not being able to directly switch between list timelines in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10973))
- Fix media sensitivity not being maintained in delete & redraft in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10980))
- Fix emoji picker being always displayed in web UI ([noellabo](https://www.okglobalcoinsg.com//pull/10979), [yuzulabo](https://www.okglobalcoinsg.com//pull/10801), [wcpaez](https://www.okglobalcoinsg.com//pull/10978))
- Fix potential private status leak through caching ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10969))
- Fix refreshing featured toots when the new collection is empty in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10971))
- Fix undoing domain block also undoing individual moderation on users from before the domain block ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10660))
- Fix time not being local in the audit log ([yuzulabo](https://www.okglobalcoinsg.com//pull/10751))
- Fix statuses removed by moderation re-appearing on subsequent fetches ([Kjwon15](https://www.okglobalcoinsg.com//pull/10732))
- Fix misattribution of inlined announces if `attributedTo` isn't present in ActivityPub ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10967))
- Fix `GET /api/v1/polls/:id` not requiring authentication for non-public polls ([Gargron](https://www.okglobalcoinsg.com//pull/10960))
- Fix handling of blank poll options in ActivityPub ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10946))
- Fix avatar preview aspect ratio on edit profile page ([Kjwon15](https://www.okglobalcoinsg.com//pull/10931))
- Fix web push notifications not being sent for polls ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10864))
- Fix cut off letters in last paragraph of statuses in web UI ([ariasuni](https://www.okglobalcoinsg.com//pull/10821))
- Fix list not being automatically unpinned when it returns 404 in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/11045))
- Fix login sometimes redirecting to paths that are not pages ([Gargron](https://www.okglobalcoinsg.com//pull/11019))

## [2.8.4] - 2019-05-24
### Fixed

- Fix delivery not retrying on some inbox errors that should be retriable ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10812))
- Fix unnecessary 5 minute cooldowns on signature verifications in some cases ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10813))
- Fix possible race condition when processing statuses ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10815))

### Security

- Require specific OAuth scopes for specific endpoints of the streaming API, instead of merely requiring a token for all endpoints, and allow using WebSockets protocol negotiation to specify the access token instead of using a query string ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10818))

## [2.8.3] - 2019-05-19
### Added

- Add `og:image:alt` OpenGraph tag ([BenLubar](https://www.okglobalcoinsg.com//pull/10779))
- Add clickable area below avatar in statuses in web UI ([Dar13](https://www.okglobalcoinsg.com//pull/10766))
- Add crossed-out eye icon on account gallery in web UI ([Kjwon15](https://www.okglobalcoinsg.com//pull/10715))
- Add media description tooltip to thumbnails in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10713))

### Changed

- Change "mark as sensitive" button into a checkbox for clarity ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10748))

### Fixed

- Fix bug allowing users to publicly boost their private statuses ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10775), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10783))
- Fix performance in formatter by a little ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10765))
- Fix some colors in the light theme ([yuzulabo](https://www.okglobalcoinsg.com//pull/10754))
- Fix some colors of the high contrast theme ([yuzulabo](https://www.okglobalcoinsg.com//pull/10711))
- Fix ambivalent active state of poll refresh button in web UI ([MaciekBaron](https://www.okglobalcoinsg.com//pull/10720))
- Fix duplicate posting being possible from web UI ([hinaloe](https://www.okglobalcoinsg.com//pull/10785))
- Fix "invited by" not showing up in admin UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10791))

## [2.8.2] - 2019-05-05
### Added

- Add `SOURCE_TAG` environment variable ([ushitora-anqou](https://www.okglobalcoinsg.com//pull/10698))

### Fixed

- Fix cropped hero image on frontpage ([BaptisteGelez](https://www.okglobalcoinsg.com//pull/10702))
- Fix blurhash gem not compiling on some operating systems ([Gargron](https://www.okglobalcoinsg.com//pull/10700))
- Fix unexpected CSS animations in some browsers ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10699))
- Fix closing video modal scrolling timelines to top ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10695))

## [2.8.1] - 2019-05-04
### Added

- Add link to existing domain block when trying to block an already-blocked domain ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10663))
- Add button to view context to media modal when opened from account gallery in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10676))
- Add ability to create multiple-choice polls in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10603))
- Add `GITHUB_REPOSITORY` and `SOURCE_BASE_URL` environment variables ([rosylilly](https://www.okglobalcoinsg.com//pull/10600))
- Add `/interact/` paths to `robots.txt` ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10666))
- Add `blurhash` to the Attachment entity in the REST API ([Gargron](https://www.okglobalcoinsg.com//pull/10630))

### Changed

- Change hidden media to be shown as a blurhash-based colorful gradient instead of a black box in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10630))
- Change rejected media to be shown as a blurhash-based gradient instead of a list of filenames in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10630))
- Change e-mail whitelist/blacklist to not be checked when invited ([Gargron](https://www.okglobalcoinsg.com//pull/10683))
- Change cache header of REST API results to no-cache ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10655))
- Change the "mark media as sensitive" button to be more obvious in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10673), [Gargron](https://www.okglobalcoinsg.com//pull/10682))
- Change account gallery in web UI to display 3 columns, open media modal ([Gargron](https://www.okglobalcoinsg.com//pull/10667), [Gargron](https://www.okglobalcoinsg.com//pull/10674))

### Fixed

- Fix LDAP/PAM/SAML/CAS users not being pre-approved ([Gargron](https://www.okglobalcoinsg.com//pull/10621))
- Fix accounts created through tootctl not being always pre-approved ([Gargron](https://www.okglobalcoinsg.com//pull/10684))
- Fix Sidekiq retrying ActivityPub processing jobs that fail validation ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10614))
- Fix toots not being scrolled into view sometimes through keyboard selection ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10593))
- Fix expired invite links being usable to bypass approval mode ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10657))
- Fix not being able to save e-mail preference for new pending accounts ([Gargron](https://www.okglobalcoinsg.com//pull/10622))
- Fix upload progressbar when image resizing is involved ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10632))
- Fix block action not automatically cancelling pending follow request ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10633))
- Fix stoplight logging to stderr separate from Rails logger ([Gargron](https://www.okglobalcoinsg.com//pull/10624))
- Fix sign up button not saying sign up when invite is used ([Gargron](https://www.okglobalcoinsg.com//pull/10623))
- Fix health checks in Docker Compose configuration ([fabianonline](https://www.okglobalcoinsg.com//pull/10553))
- Fix modal items not being scrollable on touch devices ([kedamaDQ](https://www.okglobalcoinsg.com//pull/10605))
- Fix Keybase configuration using wrong domain when a web domain is used ([BenLubar](https://www.okglobalcoinsg.com//pull/10565))
- Fix avatar GIFs not being animated on-hover on public profiles ([hyenagirl64](https://www.okglobalcoinsg.com//pull/10549))
- Fix OpenGraph parser not understanding some valid property meta tags ([da2x](https://www.okglobalcoinsg.com//pull/10604))
- Fix wrong fonts being displayed when Roboto is installed on user's machine ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10594))
- Fix confirmation modals being too narrow for a secondary action button ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10586))

## [2.8.0] - 2019-04-10
### Added

- Add polls ([Gargron](https://www.okglobalcoinsg.com//pull/10111), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10155), [Gargron](https://www.okglobalcoinsg.com//pull/10184), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10196), [Gargron](https://www.okglobalcoinsg.com//pull/10248), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10255), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10322), [Gargron](https://www.okglobalcoinsg.com//pull/10138), [Gargron](https://www.okglobalcoinsg.com//pull/10139), [Gargron](https://www.okglobalcoinsg.com//pull/10144), [Gargron](https://www.okglobalcoinsg.com//pull/10145),[Gargron](https://www.okglobalcoinsg.com//pull/10146), [Gargron](https://www.okglobalcoinsg.com//pull/10148), [Gargron](https://www.okglobalcoinsg.com//pull/10151), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10150), [Gargron](https://www.okglobalcoinsg.com//pull/10168), [Gargron](https://www.okglobalcoinsg.com//pull/10165), [Gargron](https://www.okglobalcoinsg.com//pull/10172), [Gargron](https://www.okglobalcoinsg.com//pull/10170), [Gargron](https://www.okglobalcoinsg.com//pull/10171), [Gargron](https://www.okglobalcoinsg.com//pull/10186), [Gargron](https://www.okglobalcoinsg.com//pull/10189), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10200), [rinsuki](https://www.okglobalcoinsg.com//pull/10203), [Gargron](https://www.okglobalcoinsg.com//pull/10213), [Gargron](https://www.okglobalcoinsg.com//pull/10246), [Gargron](https://www.okglobalcoinsg.com//pull/10265), [Gargron](https://www.okglobalcoinsg.com//pull/10261), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10333), [Gargron](https://www.okglobalcoinsg.com//pull/10352), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10140), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10142), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10141), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10162), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10161), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10158), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10156), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10160), [Gargron](https://www.okglobalcoinsg.com//pull/10185), [Gargron](https://www.okglobalcoinsg.com//pull/10188), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10195), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10208), [Gargron](https://www.okglobalcoinsg.com//pull/10187), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10214), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10209))
- Add follows & followers managing UI ([Gargron](https://www.okglobalcoinsg.com//pull/10268), [Gargron](https://www.okglobalcoinsg.com//pull/10308), [Gargron](https://www.okglobalcoinsg.com//pull/10404), [Gargron](https://www.okglobalcoinsg.com//pull/10293))
- Add identity proof integration with Keybase ([Gargron](https://www.okglobalcoinsg.com//pull/10297), [xgess](https://www.okglobalcoinsg.com//pull/10375), [Gargron](https://www.okglobalcoinsg.com//pull/10338), [Gargron](https://www.okglobalcoinsg.com//pull/10350), [Gargron](https://www.okglobalcoinsg.com//pull/10414))
- Add option to overwrite imported data instead of merging ([Gargron](https://www.okglobalcoinsg.com//pull/9962))
- Add featured hashtags to profiles ([Gargron](https://www.okglobalcoinsg.com//pull/9755), [Gargron](https://www.okglobalcoinsg.com//pull/10167), [Gargron](https://www.okglobalcoinsg.com//pull/10249), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10034))
- Add admission-based registrations mode ([Gargron](https://www.okglobalcoinsg.com//pull/10250), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10269), [Gargron](https://www.okglobalcoinsg.com//pull/10264), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10321), [Gargron](https://www.okglobalcoinsg.com//pull/10349), [Gargron](https://www.okglobalcoinsg.com//pull/10469))
- Add support for WebP uploads ([acid-chicken](https://www.okglobalcoinsg.com//pull/9879))
- Add "copy link" item to status action bars in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/9983))
- Add list title editing in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9748))
- Add a "Block & Report" button to the block confirmation dialog in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10360))
- Add disappointed elephant when the page crashes in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10275))
- Add ability to upload multiple files at once in web UI ([tmm576](https://www.okglobalcoinsg.com//pull/9856))
- Add indication when you are not allowed to follow an account in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10420), [Gargron](https://www.okglobalcoinsg.com//pull/10491))
- Add validations to admin settings to catch common mistakes ([Gargron](https://www.okglobalcoinsg.com//pull/10348), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10354))
- Add `type`, `limit`, `offset`, `min_id`, `max_id`, `account_id` to search API ([Gargron](https://www.okglobalcoinsg.com//pull/10091))
- Add a preferences API so apps can share basic behaviours ([Gargron](https://www.okglobalcoinsg.com//pull/10109))
- Add `visibility` param to reblog REST API ([Gargron](https://www.okglobalcoinsg.com//pull/9851), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10302))
- Add `allowfullscreen` attribute to OEmbed iframe ([rinsuki](https://www.okglobalcoinsg.com//pull/10370))
- Add `blocked_by` relationship to the REST API ([Gargron](https://www.okglobalcoinsg.com//pull/10373))
- Add `tootctl statuses remove` to sweep unreferenced statuses ([Gargron](https://www.okglobalcoinsg.com//pull/10063))
- Add `tootctl search deploy` to avoid ugly rake task syntax ([Gargron](https://www.okglobalcoinsg.com//pull/10403))
- Add `tootctl self-destruct` to shut down server gracefully ([Gargron](https://www.okglobalcoinsg.com//pull/10367))
- Add option to hide application used to toot ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9897), [rinsuki](https://www.okglobalcoinsg.com//pull/9994), [hinaloe](https://www.okglobalcoinsg.com//pull/10086))
- Add `DB_SSLMODE` configuration variable ([sascha-sl](https://www.okglobalcoinsg.com//pull/10210))
- Add click-to-copy UI to invites page ([Gargron](https://www.okglobalcoinsg.com//pull/10259))
- Add self-replies fetching ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10106), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10128), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10175), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10201))
- Add rate limit for media proxy requests ([Gargron](https://www.okglobalcoinsg.com//pull/10490))
- Add `tootctl emoji purge` ([Gargron](https://www.okglobalcoinsg.com//pull/10481))
- Add `tootctl accounts approve` ([Gargron](https://www.okglobalcoinsg.com//pull/10480))
- Add `tootctl accounts reset-relationships` ([noellabo](https://www.okglobalcoinsg.com//pull/10483))

### Changed

- Change design of landing page ([Gargron](https://www.okglobalcoinsg.com//pull/10232), [Gargron](https://www.okglobalcoinsg.com//pull/10260), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10284), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10291), [koyuawsmbrtn](https://www.okglobalcoinsg.com//pull/10356), [Gargron](https://www.okglobalcoinsg.com//pull/10245))
- Change design of profile column in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10337), [Aditoo17](https://www.okglobalcoinsg.com//pull/10387), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10390), [mayaeh](https://www.okglobalcoinsg.com//pull/10379), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10411))
- Change language detector threshold from 140 characters to 4 words ([Gargron](https://www.okglobalcoinsg.com//pull/10376))
- Change language detector to always kick in for non-latin alphabets ([Gargron](https://www.okglobalcoinsg.com//pull/10276))
- Change icons of features on admin dashboard ([Gargron](https://www.okglobalcoinsg.com//pull/10366))
- Change DNS timeouts from 1s to 5s ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10238))
- Change Docker image to use Ubuntu with jemalloc ([Sir-Boops](https://www.okglobalcoinsg.com//pull/10100), [BenLubar](https://www.okglobalcoinsg.com//pull/10212))
- Change public pages to be cacheable by proxies ([BenLubar](https://www.okglobalcoinsg.com//pull/9059))
- Change the 410 gone response for suspended accounts to be cacheable by proxies ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10339))
- Change web UI to not empty timeline of blocked users on block ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10359))
- Change JSON serializer to remove unused `@context` values ([Gargron](https://www.okglobalcoinsg.com//pull/10378))
- Change GIFV file size limit to be the same as for other videos ([rinsuki](https://www.okglobalcoinsg.com//pull/9924))
- Change Webpack to not use @babel/preset-env to compile node_modules ([ykzts](https://www.okglobalcoinsg.com//pull/10289))
- Change web UI to use new Web Share Target API ([gol-cha](https://www.okglobalcoinsg.com//pull/9963))
- Change ActivityPub reports to have persistent URIs ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10303))
- Change `tootctl accounts cull --dry-run` to list accounts that would be deleted ([BenLubar](https://www.okglobalcoinsg.com//pull/10460))
- Change format of CSV exports of follows and mutes to include extra settings ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10495), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10335))
- Change ActivityPub collections to be cacheable by proxies ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10467))
- Change REST API and public profiles to not return follows/followers for users that have blocked you ([Gargron](https://www.okglobalcoinsg.com//pull/10491))
- Change the groupings of menu items in settings navigation ([Gargron](https://www.okglobalcoinsg.com//pull/10533))

### Removed

- Remove zopfli compression to speed up Webpack from 6min to 1min ([nolanlawson](https://www.okglobalcoinsg.com//pull/10288))
- Remove stats.json generation to speed up Webpack ([nolanlawson](https://www.okglobalcoinsg.com//pull/10290))

### Fixed

- Fix public timelines being broken by new toots when they are not mounted in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10131))
- Fix quick filter settings not being saved when selecting a different filter in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10296))
- Fix remote interaction dialogs being indexed by search engines ([Gargron](https://www.okglobalcoinsg.com//pull/10240))
- Fix maxed-out invites not showing up as expired in UI ([Gargron](https://www.okglobalcoinsg.com//pull/10274))
- Fix scrollbar styles on compose textarea ([Gargron](https://www.okglobalcoinsg.com//pull/10292))
- Fix timeline merge workers being queued for remote users ([Gargron](https://www.okglobalcoinsg.com//pull/10355))
- Fix alternative relay support regression ([Gargron](https://www.okglobalcoinsg.com//pull/10398))
- Fix trying to fetch keys of unknown accounts on a self-delete from them ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10326))
- Fix CAS `:service_validate_url` option ([enewhuis](https://www.okglobalcoinsg.com//pull/10328))
- Fix race conditions when creating backups ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10234))
- Fix whitespace not being stripped out of username before validation ([aurelien-reeves](https://www.okglobalcoinsg.com//pull/10239))
- Fix n+1 query when deleting status ([Gargron](https://www.okglobalcoinsg.com//pull/10247))
- Fix exiting follows not being rejected when suspending a remote account ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10230))
- Fix the underlying button element in a disabled icon button not being disabled ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10194))
- Fix race condition when streaming out deleted statuses ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10280))
- Fix performance of admin federation UI by caching account counts ([Gargron](https://www.okglobalcoinsg.com//pull/10374))
- Fix JS error on pages that don't define a CSRF token ([hinaloe](https://www.okglobalcoinsg.com//pull/10383))
- Fix `tootctl accounts cull` sometimes removing accounts that are temporarily unreachable ([BenLubar](https://www.okglobalcoinsg.com//pull/10460))

## [2.7.4] - 2019-03-05
### Fixed

- Fix web UI not cleaning up notifications after block ([Gargron](https://www.okglobalcoinsg.com//pull/10108))
- Fix redundant HTTP requests when resolving private statuses ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10115))
- Fix performance of account media query ([abcang](https://www.okglobalcoinsg.com//pull/10121))
- Fix mention processing for unknown accounts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10125))
- Fix getting started column not scrolling on short screens ([trwnh](https://www.okglobalcoinsg.com//pull/10075))
- Fix direct messages pagination in the web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10126))
- Fix serialization of Announce activities ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10129))
- Fix home timeline perpetually reloading when empty in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/10130))
- Fix lists export ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10136))
- Fix edit profile page crash for suspended-then-unsuspended users ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10178))

## [2.7.3] - 2019-02-23
### Added

- Add domain filter to the admin federation page ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10071))
- Add quick link from admin account view to block/unblock instance ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10073))

### Fixed

- Fix video player width not being updated to fit container width ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10069))
- Fix domain filter being shown in admin page when local filter is active ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10074))
- Fix crash when conversations have no valid participants ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10078))
- Fix error when performing admin actions on no statuses ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10094))

### Changed

- Change custom emojis to randomize stored file name ([hinaloe](https://www.okglobalcoinsg.com//pull/10090))

## [2.7.2] - 2019-02-17
### Added

- Add support for IPv6 in e-mail validation ([zoc](https://www.okglobalcoinsg.com//pull/10009))
- Add record of IP address used for signing up ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10026))
- Add tight rate-limit for API deletions (30 per 30 minutes) ([Gargron](https://www.okglobalcoinsg.com//pull/10042))
- Add support for embedded `Announce` objects attributed to the same actor ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9998), [Gargron](https://www.okglobalcoinsg.com//pull/10065))
- Add spam filter for `Create` and `Announce` activities ([Gargron](https://www.okglobalcoinsg.com//pull/10005), [Gargron](https://www.okglobalcoinsg.com//pull/10041), [Gargron](https://www.okglobalcoinsg.com//pull/10062))
- Add `registrations` attribute to `GET /api/v1/instance` ([Gargron](https://www.okglobalcoinsg.com//pull/10060))
- Add `vapid_key` to `POST /api/v1/apps` and `GET /api/v1/apps/verify_credentials` ([Gargron](https://www.okglobalcoinsg.com//pull/10058))

### Fixed

- Fix link color and add link underlines in high-contrast theme ([Gargron](https://www.okglobalcoinsg.com//pull/9949), [Gargron](https://www.okglobalcoinsg.com//pull/10028))
- Fix unicode characters in URLs not being linkified ([JMendyk](https://www.okglobalcoinsg.com//pull/8447), [hinaloe](https://www.okglobalcoinsg.com//pull/9991))
- Fix URLs linkifier grabbing ending quotation as part of the link ([Gargron](https://www.okglobalcoinsg.com//pull/9997))
- Fix authorized applications page design ([rinsuki](https://www.okglobalcoinsg.com//pull/9969))
- Fix custom emojis not showing up in share page emoji picker ([rinsuki](https://www.okglobalcoinsg.com//pull/9970))
- Fix too liberal application of whitespace in toots ([trwnh](https://www.okglobalcoinsg.com//pull/9968))
- Fix misleading e-mail hint being displayed in admin view ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9973))
- Fix tombstones not being cleared out ([abcang](https://www.okglobalcoinsg.com//pull/9978))
- Fix some timeline jumps ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9982), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/10001), [rinsuki](https://www.okglobalcoinsg.com//pull/10046))
- Fix content warning input taking keyboard focus even when hidden ([hinaloe](https://www.okglobalcoinsg.com//pull/10017))
- Fix hashtags select styling in default and high-contrast themes ([Gargron](https://www.okglobalcoinsg.com//pull/10029))
- Fix style regressions on landing page ([Gargron](https://www.okglobalcoinsg.com//pull/10030))
- Fix hashtag column not subscribing to stream on mount ([Gargron](https://www.okglobalcoinsg.com//pull/10040))
- Fix relay enabling/disabling not resetting inbox availability status ([Gargron](https://www.okglobalcoinsg.com//pull/10048))
- Fix mutes, blocks, domain blocks and follow requests not paginating ([Gargron](https://www.okglobalcoinsg.com//pull/10057))
- Fix crash on public hashtag pages when streaming fails ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10061))

### Changed

- Change icon for unlisted visibility level ([clarcharr](https://www.okglobalcoinsg.com//pull/9952))
- Change queue of actor deletes from push to pull for non-follower recipients ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/10016))
- Change robots.txt to exclude media proxy URLs ([nightpool](https://www.okglobalcoinsg.com//pull/10038))
- Change upload description input to allow line breaks ([BenLubar](https://www.okglobalcoinsg.com//pull/10036))
- Change `dist/mastodon-streaming.service` to recommend running node without intermediary npm command ([nolanlawson](https://www.okglobalcoinsg.com//pull/10032))
- Change conversations to always show names of other participants ([Gargron](https://www.okglobalcoinsg.com//pull/10047))
- Change buttons on timeline preview to open the interaction dialog ([Gargron](https://www.okglobalcoinsg.com//pull/10054))
- Change error graphic to hover-to-play ([Gargron](https://www.okglobalcoinsg.com//pull/10055))

## [2.7.1] - 2019-01-28
### Fixed

- Fix SSO authentication not working due to missing agreement boolean ([Gargron](https://www.okglobalcoinsg.com//pull/9915))
- Fix slow fallback of CopyAccountStats migration setting stats to 0 ([Gargron](https://www.okglobalcoinsg.com//pull/9930))
- Fix wrong command in migration error message ([angristan](https://www.okglobalcoinsg.com//pull/9877))
- Fix initial value of volume slider in video player and handle volume changes ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9929))
- Fix missing hotkeys for notifications ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9927))
- Fix being able to attach unattached media created by other users ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9921))
- Fix unrescued SSL error during link verification ([renatolond](https://www.okglobalcoinsg.com//pull/9914))
- Fix Firefox scrollbar color regression ([trwnh](https://www.okglobalcoinsg.com//pull/9908))
- Fix scheduled status with media immediately creating a status ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9894))
- Fix missing strong style for landing page description ([Kjwon15](https://www.okglobalcoinsg.com//pull/9892))

## [2.7.0] - 2019-01-20
### Added

- Add link for adding a user to a list from their profile ([namelessGonbai](https://www.okglobalcoinsg.com//pull/9062))
- Add joining several hashtags in a single column ([gdpelican](https://www.okglobalcoinsg.com//pull/8904))
- Add volume sliders for videos ([sumdog](https://www.okglobalcoinsg.com//pull/9366))
- Add a tooltip explaining what a locked account is ([pawelngei](https://www.okglobalcoinsg.com//pull/9403))
- Add preloaded cache for common JSON-LD contexts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9412))
- Add profile directory ([Gargron](https://www.okglobalcoinsg.com//pull/9427))
- Add setting to not group reblogs in home feed ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9248))
- Add admin ability to remove a user's header image ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9495))
- Add account hashtags to ActivityPub actor JSON ([Gargron](https://www.okglobalcoinsg.com//pull/9450))
- Add error message for avatar image that's too large ([sumdog](https://www.okglobalcoinsg.com//pull/9518))
- Add notification quick-filter bar ([pawelngei](https://www.okglobalcoinsg.com//pull/9399))
- Add new first-time tutorial ([Gargron](https://www.okglobalcoinsg.com//pull/9531))
- Add moderation warnings ([Gargron](https://www.okglobalcoinsg.com//pull/9519))
- Add emoji codepoint mappings for v11.0 ([Gargron](https://www.okglobalcoinsg.com//pull/9618))
- Add REST API for creating an account ([Gargron](https://www.okglobalcoinsg.com//pull/9572))
- Add support for Malayalam in language filter ([tachyons](https://www.okglobalcoinsg.com//pull/9624))
- Add exclude_reblogs option to account statuses API ([Gargron](https://www.okglobalcoinsg.com//pull/9640))
- Add local followers page to admin account UI ([chr-1x](https://www.okglobalcoinsg.com//pull/9610))
- Add healthcheck commands to docker-compose.yml ([BenLubar](https://www.okglobalcoinsg.com//pull/9143))
- Add handler for Move activity to migrate followers ([Gargron](https://www.okglobalcoinsg.com//pull/9629))
- Add CSV export for lists and domain blocks ([Gargron](https://www.okglobalcoinsg.com//pull/9677))
- Add `tootctl accounts follow ACCT` ([Gargron](https://www.okglobalcoinsg.com//pull/9414))
- Add scheduled statuses ([Gargron](https://www.okglobalcoinsg.com//pull/9706))
- Add immutable caching for S3 objects ([nolanlawson](https://www.okglobalcoinsg.com//pull/9722))
- Add cache to custom emojis API ([Gargron](https://www.okglobalcoinsg.com//pull/9732))
- Add preview cards to non-detailed statuses on public pages ([Gargron](https://www.okglobalcoinsg.com//pull/9714))
- Add `mod` and `moderator` to list of default reserved usernames ([Gargron](https://www.okglobalcoinsg.com//pull/9713))
- Add quick links to the admin interface in the web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8545))
- Add `tootctl domains crawl` ([Gargron](https://www.okglobalcoinsg.com//pull/9809))
- Add attachment list fallback to public pages ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9780))
- Add `tootctl --version` ([Gargron](https://www.okglobalcoinsg.com//pull/9835))
- Add information about how to opt-in to the directory on the directory ([Gargron](https://www.okglobalcoinsg.com//pull/9834))
- Add timeouts for S3 ([Gargron](https://www.okglobalcoinsg.com//pull/9842))
- Add support for non-public reblogs from ActivityPub ([Gargron](https://www.okglobalcoinsg.com//pull/9841))
- Add sending of `Reject` activity when sending a `Block` activity ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9811))

### Changed

- Temporarily pause timeline if mouse moved recently ([lmorchard](https://www.okglobalcoinsg.com//pull/9200))
- Change the password form order ([mayaeh](https://www.okglobalcoinsg.com//pull/9267))
- Redesign admin UI for accounts ([Gargron](https://www.okglobalcoinsg.com//pull/9340), [Gargron](https://www.okglobalcoinsg.com//pull/9643))
- Redesign admin UI for instances/domain blocks ([Gargron](https://www.okglobalcoinsg.com//pull/9645))
- Swap avatar and header input fields in profile page ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9271))
- When posting in mobile mode, go back to previous history location ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9502))
- Split out is_changing_upload from is_submitting ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9536))
- Back to the getting-started when pins the timeline. ([kedamaDQ](https://www.okglobalcoinsg.com//pull/9561))
- Allow unauthenticated REST API access to GET /api/v1/accounts/:id/statuses ([Gargron](https://www.okglobalcoinsg.com//pull/9573))
- Limit maximum visibility of local silenced users to unlisted ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9583))
- Change API error message for unconfirmed accounts ([noellabo](https://www.okglobalcoinsg.com//pull/9625))
- Change the icon to "reply-all" when it's a reply to other accounts ([mayaeh](https://www.okglobalcoinsg.com//pull/9378))
- Do not ignore federated reports targeting already-reported accounts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9534))
- Upgrade default Ruby version to 2.6.0 ([Gargron](https://www.okglobalcoinsg.com//pull/9688))
- Change e-mail digest frequency ([Gargron](https://www.okglobalcoinsg.com//pull/9689))
- Change Docker images for Tor support in docker-compose.yml ([Sir-Boops](https://www.okglobalcoinsg.com//pull/9438))
- Display fallback link card thumbnail when none is given ([Gargron](https://www.okglobalcoinsg.com//pull/9715))
- Change account bio length validation to ignore mention domains and URLs ([Gargron](https://www.okglobalcoinsg.com//pull/9717))
- Use configured contact user for "anonymous" federation activities ([yukimochi](https://www.okglobalcoinsg.com//pull/9661))
- Change remote interaction dialog to use specific actions instead of generic "interact" ([Gargron](https://www.okglobalcoinsg.com//pull/9743))
- Always re-fetch public key when signature verification fails to support blind key rotation ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9667))
- Make replies to boosts impossible, connect reply to original status instead ([valerauko](https://www.okglobalcoinsg.com//pull/9129))
- Change e-mail MX validation to check both A and MX records against blacklist ([Gargron](https://www.okglobalcoinsg.com//pull/9489))
- Hide floating action button on search and getting started pages ([tmm576](https://www.okglobalcoinsg.com//pull/9826))
- Redesign public hashtag page to use a masonry layout ([Gargron](https://www.okglobalcoinsg.com//pull/9822))
- Use `summary` as summary instead of content warning for converted ActivityPub objects ([Gargron](https://www.okglobalcoinsg.com//pull/9823))
- Display a double reply arrow on public pages for toots that are replies ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9808))
- Change admin UI right panel size to be wider ([Kjwon15](https://www.okglobalcoinsg.com//pull/9768))

### Removed

- Remove links to bridge.joinmastodon.org (non-functional) ([Gargron](https://www.okglobalcoinsg.com//pull/9608))
- Remove LD-Signatures from activities that do not need them ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9659))

### Fixed

- Remove unused computation of reblog references from updateTimeline ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9244))
- Fix loaded embeds resetting if a status arrives from API again ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9270))
- Fix race condition causing shallow status with only a "favourited" attribute ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9272))
- Remove intermediary arrays when creating hash maps from results ([Gargron](https://www.okglobalcoinsg.com//pull/9291))
- Extract counters from accounts table to account_stats table to improve performance ([Gargron](https://www.okglobalcoinsg.com//pull/9295))
- Change identities id column to a bigint ([Gargron](https://www.okglobalcoinsg.com//pull/9371))
- Fix conversations API pagination ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9407))
- Improve account suspension speed and completeness ([Gargron](https://www.okglobalcoinsg.com//pull/9290))
- Fix thread depth computation in statuses_controller ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9426))
- Fix database deadlocks by moving account stats update outside transaction ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9437))
- Escape HTML in profile name preview in profile settings ([pawelngei](https://www.okglobalcoinsg.com//pull/9446))
- Use same CORS policy for /@:username and /users/:username ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9485))
- Make custom emoji domains case insensitive ([Esteth](https://www.okglobalcoinsg.com//pull/9474))
- Various fixes to scrollable lists and media gallery ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9501))
- Fix bootsnap cache directory being declared relatively ([Gargron](https://www.okglobalcoinsg.com//pull/9511))
- Fix timeline pagination in the web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9516))
- Fix padding on dropdown elements in preferences ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9517))
- Make avatar and headers respect GIF autoplay settings ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9515))
- Do no retry Web Push workers if the server returns a 4xx response ([Gargron](https://www.okglobalcoinsg.com//pull/9434))
- Minor scrollable list fixes ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9551))
- Ignore low-confidence CharlockHolmes guesses when parsing link cards ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9510))
- Fix `tootctl accounts rotate` not updating public keys ([Gargron](https://www.okglobalcoinsg.com//pull/9556))
- Fix CSP / X-Frame-Options for media players ([jomo](https://www.okglobalcoinsg.com//pull/9558))
- Fix unnecessary loadMore calls when the end of a timeline has been reached ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9581))
- Skip mailer job retries when a record no longer exists ([Gargron](https://www.okglobalcoinsg.com//pull/9590))
- Fix composer not getting focus after reply confirmation dialog ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9602))
- Fix signature verification stoplight triggering on non-timeout errors ([Gargron](https://www.okglobalcoinsg.com//pull/9617))
- Fix ThreadResolveWorker getting queued with invalid URLs ([Gargron](https://www.okglobalcoinsg.com//pull/9628))
- Fix crash when clearing uninitialized timeline ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9662))
- Avoid duplicate work by merging ReplyDistributionWorker into DistributionWorker ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9660))
- Skip full text search if it fails, instead of erroring out completely ([Kjwon15](https://www.okglobalcoinsg.com//pull/9654))
- Fix profile metadata links not verifying correctly sometimes ([shrft](https://www.okglobalcoinsg.com//pull/9673))
- Ensure blocked user unfollows blocker if Block/Undo-Block activities are processed out of order ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9687))
- Fix unreadable text color in report modal for some statuses ([Gargron](https://www.okglobalcoinsg.com//pull/9716))
- Stop GIFV timeline preview explicitly when it's opened in modal ([kedamaDQ](https://www.okglobalcoinsg.com//pull/9749))
- Fix scrollbar width compensation ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9824))
- Fix race conditions when processing deleted toots ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9815))
- Fix SSO issues on WebKit browsers by disabling Same-Site cookie again ([moritzheiber](https://www.okglobalcoinsg.com//pull/9819))
- Fix empty OEmbed error ([renatolond](https://www.okglobalcoinsg.com//pull/9807))
- Fix drag & drop modal not disappearing sometimes ([hinaloe](https://www.okglobalcoinsg.com//pull/9797))
- Fix statuses with content warnings being displayed in web push notifications sometimes ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9778))
- Fix scroll-to-detailed status not working on public pages ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9773))
- Fix media modal loading indicator ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9771))
- Fix hashtag search results not having a permalink fallback in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9810))
- Fix slightly cropped font on settings page dropdowns when using system font ([ariasuni](https://www.okglobalcoinsg.com//pull/9839))
- Fix not being able to drag & drop text into forms ([tmm576](https://www.okglobalcoinsg.com//pull/9840))

### Security

- Sanitize and sandbox toot embeds in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9552))
- Add tombstones for remote statuses to prevent replay attacks ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9830))

## [2.6.5] - 2018-12-01
### Changed

- Change lists to display replies to others on the list and list owner ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9324))

### Fixed

- Fix failures caused by commonly-used JSON-LD contexts being unavailable ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9412))

## [2.6.4] - 2018-11-30
### Fixed

- Fix yarn dependencies not installing due to yanked event-stream package ([Gargron](https://www.okglobalcoinsg.com//pull/9401))

## [2.6.3] - 2018-11-30
### Added

- Add hyphen to characters allowed in remote usernames ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9345))

### Changed

- Change server user count to exclude suspended accounts ([Gargron](https://www.okglobalcoinsg.com//pull/9380))

### Fixed

- Fix ffmpeg processing sometimes stalling due to overfilled stdout buffer ([hugogameiro](https://www.okglobalcoinsg.com//pull/9368))
- Fix missing DNS records raising the wrong kind of exception ([Gargron](https://www.okglobalcoinsg.com//pull/9379))
- Fix already queued deliveries still trying to reach inboxes marked as unavailable ([Gargron](https://www.okglobalcoinsg.com//pull/9358))

### Security

- Fix TLS handshake timeout not being enforced ([Gargron](https://www.okglobalcoinsg.com//pull/9381))

## [2.6.2] - 2018-11-23
### Added

- Add Page to whitelisted ActivityPub types ([mbajur](https://www.okglobalcoinsg.com//pull/9188))
- Add 20px to column width in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/9227))
- Add amount of freed disk space in `tootctl media remove` ([Gargron](https://www.okglobalcoinsg.com//pull/9229), [Gargron](https://www.okglobalcoinsg.com//pull/9239), [mayaeh](https://www.okglobalcoinsg.com//pull/9288))
- Add "Show thread" link to self-replies ([Gargron](https://www.okglobalcoinsg.com//pull/9228))

### Changed

- Change order of Atom and RSS links so Atom is first ([Alkarex](https://www.okglobalcoinsg.com//pull/9302))
- Change Nginx configuration for Nanobox apps ([danhunsaker](https://www.okglobalcoinsg.com//pull/9310))
- Change the follow action to appear instant in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/9220))
- Change how the ActiveRecord connection is instantiated in on_worker_boot ([Gargron](https://www.okglobalcoinsg.com//pull/9238))
- Change `tootctl accounts cull` to always touch accounts so they can be skipped ([renatolond](https://www.okglobalcoinsg.com//pull/9293))
- Change mime type comparison to ignore JSON-LD profile ([valerauko](https://www.okglobalcoinsg.com//pull/9179))

### Fixed

- Fix web UI crash when conversation has no last status ([sammy8806](https://www.okglobalcoinsg.com//pull/9207))
- Fix follow limit validator reporting lower number past threshold ([Gargron](https://www.okglobalcoinsg.com//pull/9230))
- Fix form validation flash message color and input borders ([Gargron](https://www.okglobalcoinsg.com//pull/9235))
- Fix invalid twitter:player cards being displayed ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9254))
- Fix emoji update date being processed incorrectly ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9255))
- Fix playing embed resetting if status is reloaded in web UI ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9270), [Gargron](https://www.okglobalcoinsg.com//pull/9275))
- Fix web UI crash when favouriting a deleted status ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9272))
- Fix intermediary arrays being created for hash maps ([Gargron](https://www.okglobalcoinsg.com//pull/9291))
- Fix filter ID not being a string in REST API ([Gargron](https://www.okglobalcoinsg.com//pull/9303))

### Security

- Fix multiple remote account deletions being able to deadlock the database ([Gargron](https://www.okglobalcoinsg.com//pull/9292))
- Fix HTTP connection timeout of 10s not being enforced ([Gargron](https://www.okglobalcoinsg.com//pull/9329))

## [2.6.1] - 2018-10-30
### Fixed

- Fix resolving resources by URL not working due to a regression in [valerauko](https://www.okglobalcoinsg.com//pull/9132) ([Gargron](https://www.okglobalcoinsg.com//pull/9171))
- Fix reducer error in web UI when a conversation has no last status ([Gargron](https://www.okglobalcoinsg.com//pull/9173))

## [2.6.0] - 2018-10-30
### Added

- Add link ownership verification ([Gargron](https://www.okglobalcoinsg.com//pull/8703))
- Add conversations API ([Gargron](https://www.okglobalcoinsg.com//pull/8832))
- Add limit for the number of people that can be followed from one account ([Gargron](https://www.okglobalcoinsg.com//pull/8807))
- Add admin setting to customize mascot ([ashleyhull-versent](https://www.okglobalcoinsg.com//pull/8766))
- Add support for more granular ActivityPub audiences from other software, i.e. circles ([Gargron](https://www.okglobalcoinsg.com//pull/8950), [Gargron](https://www.okglobalcoinsg.com//pull/9093), [Gargron](https://www.okglobalcoinsg.com//pull/9150))
- Add option to block all reports from a domain ([Gargron](https://www.okglobalcoinsg.com//pull/8830))
- Add user preference to always expand toots marked with content warnings ([webroo](https://www.okglobalcoinsg.com//pull/8762))
- Add user preference to always hide all media ([fvh-P](https://www.okglobalcoinsg.com//pull/8569))
- Add `force_login` param to OAuth authorize page ([Gargron](https://www.okglobalcoinsg.com//pull/8655))
- Add `tootctl accounts backup` ([Gargron](https://www.okglobalcoinsg.com//pull/8642), [Gargron](https://www.okglobalcoinsg.com//pull/8811))
- Add `tootctl accounts create` ([Gargron](https://www.okglobalcoinsg.com//pull/8642), [Gargron](https://www.okglobalcoinsg.com//pull/8811))
- Add `tootctl accounts cull` ([Gargron](https://www.okglobalcoinsg.com//pull/8642), [Gargron](https://www.okglobalcoinsg.com//pull/8811))
- Add `tootctl accounts delete` ([Gargron](https://www.okglobalcoinsg.com//pull/8642), [Gargron](https://www.okglobalcoinsg.com//pull/8811))
- Add `tootctl accounts modify` ([Gargron](https://www.okglobalcoinsg.com//pull/8642), [Gargron](https://www.okglobalcoinsg.com//pull/8811))
- Add `tootctl accounts refresh` ([Gargron](https://www.okglobalcoinsg.com//pull/8642), [Gargron](https://www.okglobalcoinsg.com//pull/8811))
- Add `tootctl feeds build` ([Gargron](https://www.okglobalcoinsg.com//pull/8642), [Gargron](https://www.okglobalcoinsg.com//pull/8811))
- Add `tootctl feeds clear` ([Gargron](https://www.okglobalcoinsg.com//pull/8642), [Gargron](https://www.okglobalcoinsg.com//pull/8811))
- Add `tootctl settings registrations open` ([Gargron](https://www.okglobalcoinsg.com//pull/8642), [Gargron](https://www.okglobalcoinsg.com//pull/8811))
- Add `tootctl settings registrations close` ([Gargron](https://www.okglobalcoinsg.com//pull/8642), [Gargron](https://www.okglobalcoinsg.com//pull/8811))
- Add `min_id` param to REST API to support backwards pagination ([Gargron](https://www.okglobalcoinsg.com//pull/8736))
- Add a confirmation dialog when hitting reply and the compose box isn't empty ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8893))
- Add PostgreSQL disk space growth tracking in PGHero ([Gargron](https://www.okglobalcoinsg.com//pull/8906))
- Add button for disabling local account to report quick actions bar ([Gargron](https://www.okglobalcoinsg.com//pull/9024))
- Add Czech language ([Aditoo17](https://www.okglobalcoinsg.com//pull/8594))
- Add `same-site` (`lax`) attribute to cookies ([sorin-davidoi](https://www.okglobalcoinsg.com//pull/8626))
- Add support for styled scrollbars in Firefox Nightly ([sorin-davidoi](https://www.okglobalcoinsg.com//pull/8653))
- Add highlight to the active tab in web UI profiles ([rhoio](https://www.okglobalcoinsg.com//pull/8673))
- Add auto-focus for comment textarea in report modal ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8689))
- Add auto-focus for emoji picker's search field ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8688))
- Add nginx and systemd templates to `dist/` directory ([Gargron](https://www.okglobalcoinsg.com//pull/8770))
- Add support for `/.well-known/change-password` ([Gargron](https://www.okglobalcoinsg.com//pull/8828))
- Add option to override FFMPEG binary path ([sascha-sl](https://www.okglobalcoinsg.com//pull/8855))
- Add `dns-prefetch` tag when using different host for assets or uploads ([Gargron](https://www.okglobalcoinsg.com//pull/8942))
- Add `description` meta tag ([Gargron](https://www.okglobalcoinsg.com//pull/8941))
- Add `Content-Security-Policy` header ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8957))
- Add cache for the instance info API ([ykzts](https://www.okglobalcoinsg.com//pull/8765))
- Add suggested follows to search screen in mobile layout ([Gargron](https://www.okglobalcoinsg.com//pull/9010))
- Add CORS header to `/.well-known/*` routes ([BenLubar](https://www.okglobalcoinsg.com//pull/9083))
- Add `card` attribute to statuses returned from REST API ([Gargron](https://www.okglobalcoinsg.com//pull/9120))
- Add in-stream link preview ([Gargron](https://www.okglobalcoinsg.com//pull/9120))
- Add support for ActivityPub `Page` objects ([mbajur](https://www.okglobalcoinsg.com//pull/9121))

### Changed

- Change forms design ([Gargron](https://www.okglobalcoinsg.com//pull/8703))
- Change reports overview to group by target account ([Gargron](https://www.okglobalcoinsg.com//pull/8674))
- Change web UI to show "read more" link on overly long in-stream statuses ([lanodan](https://www.okglobalcoinsg.com//pull/8205))
- Change design of direct messages column ([Gargron](https://www.okglobalcoinsg.com//pull/8832), [Gargron](https://www.okglobalcoinsg.com//pull/9022))
- Change home timelines to exclude DMs ([Gargron](https://www.okglobalcoinsg.com//pull/8940))
- Change list timelines to exclude all replies ([cbayerlein](https://www.okglobalcoinsg.com//pull/8683))
- Change admin accounts UI default sort to most recent ([Gargron](https://www.okglobalcoinsg.com//pull/8813))
- Change documentation URL in the UI ([Gargron](https://www.okglobalcoinsg.com//pull/8898))
- Change style of success and failure messages ([Gargron](https://www.okglobalcoinsg.com//pull/8973))
- Change DM filtering to always allow DMs from staff ([qguv](https://www.okglobalcoinsg.com//pull/8993))
- Change recommended Ruby version to 2.5.3 ([zunda](https://www.okglobalcoinsg.com//pull/9003))
- Change docker-compose default to persist volumes in current directory ([Gargron](https://www.okglobalcoinsg.com//pull/9055))
- Change character counters on edit profile page to input length limit ([Gargron](https://www.okglobalcoinsg.com//pull/9100))
- Change notification filtering to always let through messages from staff ([Gargron](https://www.okglobalcoinsg.com//pull/9152))
- Change "hide boosts from user" function also hiding notifications about boosts ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9147))
- Change CSS `detailed-status__wrapper` class actually wrap the detailed status ([trwnh](https://www.okglobalcoinsg.com//pull/8547))

### Deprecated

- `GET /api/v1/timelines/direct` → `GET /api/v1/conversations` ([Gargron](https://www.okglobalcoinsg.com//pull/8832))
- `POST /api/v1/notifications/dismiss` → `POST /api/v1/notifications/:id/dismiss` ([Gargron](https://www.okglobalcoinsg.com//pull/8905))
- `GET /api/v1/statuses/:id/card` → `card` attributed included in status ([Gargron](https://www.okglobalcoinsg.com//pull/9120))

### Removed

- Remove "on this device" label in column push settings ([rhoio](https://www.okglobalcoinsg.com//pull/8704))
- Remove rake tasks in favour of tootctl commands ([Gargron](https://www.okglobalcoinsg.com//pull/8675))

### Fixed

- Fix remote statuses using instance's default locale if no language given ([Kjwon15](https://www.okglobalcoinsg.com//pull/8861))
- Fix streaming API not exiting when port or socket is unavailable ([Gargron](https://www.okglobalcoinsg.com//pull/9023))
- Fix network calls being performed in database transaction in ActivityPub handler ([Gargron](https://www.okglobalcoinsg.com//pull/8951))
- Fix dropdown arrow position ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8637))
- Fix first element of dropdowns being focused even if not using keyboard ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8679))
- Fix tootctl requiring `bundle exec` invocation ([abcang](https://www.okglobalcoinsg.com//pull/8619))
- Fix public pages not using animation preference for avatars ([renatolond](https://www.okglobalcoinsg.com//pull/8614))
- Fix OEmbed/OpenGraph cards not understanding relative URLs ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8669))
- Fix some dark emojis not having a white outline ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8597))
- Fix media description not being displayed in various media modals ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8678))
- Fix generated URLs of desktop notifications missing base URL ([GenbuHase](https://www.okglobalcoinsg.com//pull/8758))
- Fix RTL styles ([mabkenar](https://www.okglobalcoinsg.com//pull/8764), [mabkenar](https://www.okglobalcoinsg.com//pull/8767), [mabkenar](https://www.okglobalcoinsg.com//pull/8823), [mabkenar](https://www.okglobalcoinsg.com//pull/8897), [mabkenar](https://www.okglobalcoinsg.com//pull/9005), [mabkenar](https://www.okglobalcoinsg.com//pull/9007), [mabkenar](https://www.okglobalcoinsg.com//pull/9018), [mabkenar](https://www.okglobalcoinsg.com//pull/9021), [mabkenar](https://www.okglobalcoinsg.com//pull/9145), [mabkenar](https://www.okglobalcoinsg.com//pull/9146))
- Fix crash in streaming API when tag param missing ([Gargron](https://www.okglobalcoinsg.com//pull/8955))
- Fix hotkeys not working when no element is focused ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8998))
- Fix some hotkeys not working on detailed status view ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9006))
- Fix og:url on status pages ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9047))
- Fix upload option buttons only being visible on hover ([Gargron](https://www.okglobalcoinsg.com//pull/9074))
- Fix tootctl not returning exit code 1 on wrong arguments ([sascha-sl](https://www.okglobalcoinsg.com//pull/9094))
- Fix preview cards for appearing for profiles mentioned in toot ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/6934), [ClearlyClaire](https://www.okglobalcoinsg.com//pull/9158))
- Fix local accounts sometimes being duplicated as faux-remote ([Gargron](https://www.okglobalcoinsg.com//pull/9109))
- Fix emoji search when the shortcode has multiple separators ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/9124))
- Fix dropdowns sometimes being partially obscured by other elements ([kedamaDQ](https://www.okglobalcoinsg.com//pull/9126))
- Fix cache not updating when reply/boost/favourite counters or media sensitivity update ([Gargron](https://www.okglobalcoinsg.com//pull/9119))
- Fix empty display name precedence over username in web UI ([Gargron](https://www.okglobalcoinsg.com//pull/9163))
- Fix td instead of th in sessions table header ([Gargron](https://www.okglobalcoinsg.com//pull/9162))
- Fix handling of content types with profile ([valerauko](https://www.okglobalcoinsg.com//pull/9132))

## [2.5.2] - 2018-10-12
### Security

- Fix XSS vulnerability ([Gargron](https://www.okglobalcoinsg.com//pull/8959))

## [2.5.1] - 2018-10-07
### Fixed

- Fix database migrations for PostgreSQL below 9.5 ([Gargron](https://www.okglobalcoinsg.com//pull/8903))
- Fix class autoloading issue in ActivityPub Create handler ([Gargron](https://www.okglobalcoinsg.com//pull/8820))
- Fix cache statistics not being sent via statsd when statsd enabled ([ykzts](https://www.okglobalcoinsg.com//pull/8831))
- Bump puma from 3.11.4 to 3.12.0 ([dependabot[bot]](https://www.okglobalcoinsg.com//pull/8883))

### Security

- Fix some local images not having their EXIF metadata stripped on upload ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8714))
- Fix being able to enable a disabled relay via ActivityPub Accept handler ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8864))
- Bump nokogiri from 1.8.4 to 1.8.5 ([dependabot[bot]](https://www.okglobalcoinsg.com//pull/8881))
- Fix being able to report statuses not belonging to the reported account ([ClearlyClaire](https://www.okglobalcoinsg.com//pull/8916))
