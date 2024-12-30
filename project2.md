+-----------------------+-----------------+----------------------------------+
| Column Name           | Data Type      | Description                      |
+-----------------------+-----------------+----------------------------------+
| website_session_id    | BIGINT         | Unique identifier for the session |
| created_at            | DATETIME       | Session creation date and time   |
| user_id               | BIGINT         | Identifier for the user          |
| is_repeat_session     | BINARY         | Indicates if it's a repeat session |
| utm_source            | VARCHAR(45)    | Source of the traffic            |
+-----------------------+-----------------+----------------------------------+
