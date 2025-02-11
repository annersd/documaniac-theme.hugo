---
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
date: '{{ .Date }}'
draft: true
---

This is the default archetype for content pages. You can use it to create new content pages by running `hugo new content/<path>/<name>.md`.
