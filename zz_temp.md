```html

    <script>
        (function () {
            const isLocal = ['localhost', '127.0.0.1', '::1'].includes(location.hostname);
            const baseHref = isLocal ? '/' : '/${1:REPO_NAME}/';
            const base = document.createElement('base');
            base.setAttribute('href', baseHref);
            document.head.prepend(base); // insert as the first element in <head>
        })();
    </script>

```