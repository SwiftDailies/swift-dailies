---
layout: post
date: 2016-11-21
title: Init DateFormatter with format
published: true
permalink: /init-dateformatter-with-format/
---

%23%20Init%20DateFormatter%20with%20format%0A%0AInitialize%20a%20DateFormatter%20directly%20with%20a%20format%20string.%0A%0A%60%60%60%0Aextension%20DateFormatter%20%7B%0A%09convenience%20init(with%20format:%20String)%20%7B%0A%09%09self.init()%0A%09%09self.dateFormat%20%3D%20format%0A%09%7D%0A%7D%0A%60%60%60%0A%0AUse%20it%20like%20this.%0A%0A%60%60%60%0Alet%20format%20%3D%20%22YYYY-MM-dd%22%0Alet%20formatter%20%3D%20DateFormatter(with:%20format)%0Alet%20dateString%20%3D%20formatter.string(from:%20Date()