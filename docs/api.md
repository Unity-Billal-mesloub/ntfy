# API Reference

This page contains the interactive API documentation for ntfy. You can try out the API endpoints directly from this page.

## Using the API Documentation

### Server Selection

The API reference includes a server selector dropdown at the top of the page. By default, it's configured to use the **public ntfy.sh server**.

To use your own ntfy instance, edit `docs/api/openapi.yaml` and add your server URL to the `servers` section:

```yaml
servers:
  - url: https://ntfy.sh
    description: Public ntfy server
  - url: https://your-ntfy-instance.com
    description: Your custom server
```

After editing the file, rebuild the docs with `mkdocs build`.

### Authentication

Click the **Authorize** button (lock icon) in the API reference to add your access token. Use the format `Bearer <your_token>` or `Basic <base64_encoded_credentials>`.

### Try It Out

Click **Try it out** on any endpoint to test it directly. Parameters will be empty by default - enter your own values to test.

---

<script>
  // Redirect to standalone Scalar page - use absolute path from root
  var currentPath = window.location.pathname;
  // Get base path (everything before /api/)
  var basePath = currentPath.substring(0, currentPath.indexOf('/api/'));
  if (basePath === -1 || basePath === '') {
    basePath = '';
  }
  window.location.href = basePath + '/api/scalar.html';
</script>

If you are not redirected automatically, [click here to view the API Reference](api/scalar.html).