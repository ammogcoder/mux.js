# Troubleshooting Guide

## Table of Contents
- [608/708 Caption Parsing](caption-parsing)

## 608/708 Caption Parsing

**I have a stream with caption data in more than one field, but only captions from one field are being returned**

You may want to confirm the SEI NAL units are constructed according to the CEA-608 or CEA-708 specification. Specifically:

- that control codes/commands are doubled
- control codes starting from 0x14, 0x20 and ending with 0x14, 0x2f in field 1 are replaced with 0x15, 0x20 to 0x15, 0x2f when used in field 2
- control codes starting from 0x1c, 0x20 and ending with 0x1c, 0x2f in field 1 are replaced with 0x1d, 0x20 to 0x1d, 0x2f when used in field 2

[caption-parsing]: /docs/troubleshooting.md#608/708-caption-parsing