# Client API Change Log

## December 16, 2015

#### Bug Fixes

* Fixed sorting by `last_message` and paginating.
* Optimized posting conversations

## November 4, 2015

#### Bug Fixes

* The `Layer-Count` header is now returned with all collections, and not solely when there are more resources to load.
* Improved handling of WebSockets and XHR requests that involve a deleted Session Token
* The `last_message` property is now returned when a Create Conversation request returns an existing Distinct Conversation.
* Fixes overly long timeouts

#### Enhancements

* Conversations can now be sorted by `last_message.sent_at`, not just by `created_at`.
* Now supports `X-HTTP-Method-Override: PATCH` as an alternate way of issuing a PATCH request.

## October 6, 2015

Initial public release `1.0`

#### Enhancements

* Authentication
* CRUD methods on conversations, messages, and content
* Websocket notifications
* Websocket conversation and message creation methods
