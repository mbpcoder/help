# Composer Tips

### Local package development

```json
{
    "repositories": [
        {
            "type": "path",
            "url": "C:/Users/mbpcoder/Projects/my-package",
            "options": {
                "symlink": true
            }
        }
    ],
    "require": {
        "mbpcoder/my-package": "@dev"
    }
}
```
