# Composer Tips

### Local package development

```json
{
    "repositories": [
        {
            "type": "path",
            "url": "C:/Users/Bagheri/Documents/Projects/my-package",
            "options": {
                "symlink": true
            }
        }
    ],
    "require": {
        "aschmelyun/my-package": "@dev"
    }
}
```
