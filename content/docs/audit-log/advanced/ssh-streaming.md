---
date: "2016-07-03T04:02:20Z"
title: "SSH Event Streaming"
description: "Events in an audit log must be ordered"
weight: "1804"
categories: [ "Advanced Audit Logging" ]
index: ["docs/audit-log", "docs"]
icon: "replicatedCircle"
---

SSH Event Streaming allows Enterprise API users to stream events as they occur over ssh using an Enterprise API Token.


## Usage

To use the SSH event streaming feature, you'll need to start by getting an [Enterprise API token](/docs/audit-log/apis/enterprise-api#getting-an-enterprise-api-token).

To open a stream for your sandbox, connect to `tail.auditlog.replicated.com` using your Enterprise API token as the username:

```
ssh aeb1c315b9a8ed11a3f998d8e8ff@tail.auditlog.replicated.com
```

Once the connection is open, CSV events will begin to stream through stdout, and can be piped to a file or other event ingest system.

The same token can be used for multiple concurrent streaming sessions, all sessions will receive every event that occurs while they are active.

## Parameters

The streaming APIs support a few parameters that can control the format of events. The default output format is CSV, but JSON is also supported via the `format` parameter

```
ssh aeb1c315b9a8ed11a3f998d8e8ff?format=json@tail.auditlog.replicated.com
```