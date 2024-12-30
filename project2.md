<table>
  <thead>
    <tr>
      <th>Column Name</th>
      <th>Data Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>website_session_id</td>
      <td>BIGINT</td>
      <td>Unique identifier for the session</td>
    </tr>
    <tr>
      <td>created_at</td>
      <td>DATETIME</td>
      <td>Session creation date and time</td>
    </tr>
    <tr>
      <td>user_id</td>
      <td>BIGINT</td>
      <td>Identifier for the user</td>
    </tr>
    <tr>
      <td>is_repeat_session</td>
      <td>BINARY</td>
      <td>Indicates if it's a repeat session</td>
    </tr>
    <tr>
      <td>utm_source</td>
      <td>VARCHAR(45)</td>
      <td>Source of the traffic</td>
    </tr>
    <tr>
      <td>utm_campaign</td>
      <td>VARCHAR(45)</td>
      <td>Campaign name in marketing</td>
    </tr>
    <tr>
      <td>utm_content</td>
      <td>VARCHAR(45)</td>
      <td>Content identifier in marketing</td>
    </tr>
    <tr>
      <td>device_type</td>
      <td>VARCHAR(45)</td>
      <td>Type of device used</td>
    </tr>
    <tr>
      <td>http_referer</td>
      <td>VARCHAR(45)</td>
      <td>HTTP referrer link</td>
    </tr>
  </tbody>
</table>

