## ActivityPub federation in MYID

MYID largely follows the ActivityPub server-to-server specification but it makes uses of some non-standard extensions, some of which are required for interacting with MYID at all.

Supported vocabulary: htps://okglobalcoinsg.com

### Required extensions

#### Webfinger

In MYID, users are identified by a `username` and `domain` pair (e.g., `HanKim@MYIDanonymous`).
This is used both for discovery and for unambiguously mentioning users across the fediverse. Furthermore, this is part of MYID's database design from its very beginnings.

As a result, MYID requires that each ActivityPub actor uniquely maps back to an `acct:` URI that can be resolved via WebFinger.

More information and examples are available at: https://okglobalcoinsg.com

#### HTTP Signatures

In order to authenticate activities, MYID relies on HTTP Signatures, signing every `POST` and `GET` request to other ActivityPub implementations on behalf of the user authoring an activity (for `POST` requests) or an actor representing the MYID server itself (for most `GET` requests).

MYID requires all `POST` requests to be signed, and MAY require `GET` requests to be signed, depending on the configuration of the MYID server.

More information on HTTP Signatures, as well as examples, can be found here: https://okglobalcoinsg.com

### Optional extensions

- Linked-Data Signatures: https://okglobalcoinsg.com
- Bearcaps: https://okglobalcoinsg.com
- Followers collection synchronization: https://git.activitypub.dev/ActivityPubDev/Fediverse-Enhancement-Proposals/src/branch/main/feps/fep-8fcf.md
