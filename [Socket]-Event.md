# chat message
| Event        | Data    |
| ------------ | ------- |
| chat message | Message |

# room
| Event        | Data    |
| ------------ | ------- |
| room         | Updated Room |


# lastRead
Data properties

| Propert      | Data    |
| ------------ | ------- |
| roomID       | Room ID |
| memberID     | Report member id |
| messageID    | Last read message id |

```json
{
  "roomID":"5be660651a71681534245a4e",
  "messageID":"5be7edaced649e42234f0699",
  "memberID":"aaa"
}
```

# typing
| Event        | Data    |
| ------------ | ------- |
| typing       | Some member is typing message |

```json
{
  "room": "58871b877390be11d5f1ab30",
  "message": "typing content"
}
```