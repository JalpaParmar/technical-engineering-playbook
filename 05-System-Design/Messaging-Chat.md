# Design Messaging / Chat

## Requirements
One-to-one/group messaging, history, delivery/read states, multi-device use and push for offline recipients.

## Architecture
Persistent connection gateway handles realtime delivery; message service assigns durable identity/order semantics; database stores history; asynchronous pipeline handles push/analytics.

## Ordering
Define ordering scope—per conversation is more practical than global order. Sequence/server timestamps can help, but clocks alone are not a perfect ordering mechanism.

## Offline
Client reconnects with cursor/last-known sequence and reconciles missing messages. Sending uses client-generated operation identity to handle retry.

## Scale
Partition by conversation/user keys where appropriate and separate presence/ephemeral state from durable message history.
