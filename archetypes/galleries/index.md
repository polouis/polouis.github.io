---
draft: true
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
cover:
  image: '/galleries/{{.File.ContentBaseName}}/cover.jpg'
  alt: ''
---
{{< gallery >}}