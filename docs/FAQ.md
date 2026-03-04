---
title: Frequently asked questions and answers
description: Short answers and troubleshooting for Xeno Bot docs (FAQ).
tags:
  - faq
  - questions
  - answers
keywords:
  - xeno
  - bot
  - faq
  - documentation
author: Devvyyxyz
image: assets/images/faq-og.png
date: 2026-03-04
permalink: /faq/
toc: true
icon: mdi:help-circle
aliases:
  - /frequently-asked-question/
---
## Quick Answers

> **Q: How do I catch eggs?**

To catch an egg type `egg` in the configured spawn channel

> **Q: How do I see my eggs, xeno's, items & hosts?**

Run the `/inventory` command and navigate to the respected menu.

!!! warning "OpenSSL / LibreSSL"
		If you see a `NotOpenSSLWarning` referencing LibreSSL when installing
		requests/urllib3, consider upgrading your system OpenSSL or ignore the
		warning if the rest of the build succeeds. macOS users can run:

		```bash
		xcode-select --install
		brew install openssl
		```