[![GitHub license](https://img.shields.io/badge/license-FPDF-green)](https://github.com/fawno/FPDF-mirror/blob/master/LICENSE)
[![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/fawno/FPDF-mirror)](https://github.com/fawno/FPDF-mirror/tags)
[![GitHub release](https://img.shields.io/github/release/fawno/FPDF-mirror)](https://github.com/fawno/FPDF-mirror/releases)
[![Packagist](https://img.shields.io/packagist/v/fpdf-mirror/fpdf)](https://packagist.org/packages/fpdf-mirror/fpdf)
[![Packagist Downloads](https://img.shields.io/packagist/dt/fpdf-mirror/fpdf)](https://packagist.org/packages/fpdf-mirror/fpdf/stats)
[![GitHub issues](https://img.shields.io/github/issues/fawno/FPDF-mirror)](https://github.com/fawno/FPDF-mirror/issues)
[![GitHub forks](https://img.shields.io/github/forks/fawno/FPDF-mirror)](https://github.com/fawno/FPDF-mirror/network)
[![GitHub stars](https://img.shields.io/github/stars/fawno/FPDF-mirror)](https://github.com/fawno/FPDF-mirror/stargazers)

# FPDF (dev-fawno branch)

> **Temporary compatibility branch for FPDF**

This branch provides a temporary patched version of the original FPDF library for situations where compatibility issues or critical bugs affect production environments before an official upstream fix is released.

## Purpose of this branch

The **`dev-fawno`** branch exists as a short-term compatibility layer.

Its purpose is to provide:

* Fixes for new PHP version incompatibilities
* Temporary workarounds for deprecated features
* Runtime warning corrections
* Critical bug fixes affecting stability

This branch is **not intended to replace the official FPDF releases**.

It exists to bridge the gap between an issue being discovered and the official FPDF maintainer publishing a proper fix.

Once upstream resolves the issue, this branch is realigned accordingly.

## Why does this exist?

Historically, there have been situations where:

* New PHP versions introduced breaking changes
* Existing FPDF code generated warnings or errors
* Official fixes took weeks or even months to be released

For production systems, waiting is not always an option.

This branch provides a practical fallback.

## When should I use this?

Use the standard stable package by default:

```bash
composer require fpdf-mirror/fpdf
```

Only switch to **`dev-fawno`** if:

* You encounter a known compatibility issue
* Your PHP version introduces a breaking change
* A temporary patch has been announced in this branch

To switch:

```bash
composer require fpdf-mirror/fpdf dev-fawno
```

This allows you to temporarily apply the fixes without manually patching vendor files.

Once the official upstream version is released, you can return to stable:

```bash
composer require fpdf-mirror/fpdf
```

## What is FPDF?

FPDF is a PHP class which allows generating PDF files with pure PHP, without using the PDFlib library.

FPDF offers:

* Choice of measure unit, page format and margins
* Header and footer management
* Automatic page breaks
* Automatic line breaks and text justification
* Image support (JPEG, PNG and GIF)
* Colors
* Links
* TrueType, Type1 and encoding support
* Page compression

FPDF requires no extensions (except Zlib for compression and GD for GIF support).

## About this repository

This repository is a Composer-compatible mirror of the official FPDF project.

The stable branches aim to remain as close as possible to the original source.

The `dev-fawno` branch is the only branch where temporary compatibility patches may be introduced when necessary.

Official upstream source:

https://www.fpdf.org

Official documentation:

https://www.fpdf.org/en/doc/index.php

Official downloads:

https://www.fpdf.org/en/download.php

## Important notice

If you are using this branch, you should consider it a temporary solution.

Whenever an official FPDF release includes the required fix, upgrading back to the stable release is strongly recommended.
