# Matter Specification (Version 1.0)

<table>
<tbody>
  <tr>
    <td>Document:</td>
    <td>22-22349-001_Matter-1.0-Core-Specification.pdf<br>September 28, 2022</td>
  </tr>
  <tr>
    <td>Sponsored by:</td>
    <td>Connectivity Standards Alliance</td>
  </tr>
  <tr>
    <td>Accepted by:</td>
    <td>This document has been accepted for release by the Connectivity Standards Alliance Board of Directors on <strong>September 28, 2022</strong></td>
  </tr>
  <tr>
    <td>Abstract:</td>
    <td>The Matter specification defines fundamental requirements to enable an interoperable application layer solution for smart home devices over the Internet Protocol.</td>
  </tr>
  <tr>
    <td>Keywords:</td>
    <td>Referenced in Chapter 1.</td>
  </tr>
</tbody>
</table>

<p>
  Copyright © 2022 Connectivity Standards Alliance, Inc.<br>
  508 Second Street, Suite 109B Davis, CA 95616 - USA<br>
  www.csa-iot.org<br>
  All rights reserved.<br>
</p>

<p>
  Permission is granted to members of the Connectivity Standards Alliance to reproduce this document for their own use or the use of other Connectivity Standards Alliance members only, provided this notice is included. All other rights reserved. Duplication for sale, or for commercial or for-profit use is strictly prohibited without the prior written consent of the Connectivity Standards Alliance.
</p>

# Copyright Notice, License and Disclaimer

<p>
  Copyright © Connectivity Standards Alliance (2022). All Rights Reserved. The information within this document is the property of the Connectivity Standards Alliance and its use and disclosure are restricted, except as expressly set forth herein.
</p>

<p>
  Connectivity Standards Alliance hereby grants you a fully-paid, non-exclusive, nontransferable, worldwide, limited and revocable license (without the right to sublicense), under Connectivity Standards Alliance’s applicable copyright rights, to view, download, save, reproduce and use the document solely for your own internal purposes and in accordance with the terms of the license set forth herein. This license does not authorize you to, and you expressly warrant that you shall not: (a) permit others (outside your organization) to use this document; (b) post or publish this document; (c) modify, adapt, translate, or otherwise change this document in any manner or create any derivative work based on this document; (d) remove or modify any notice or label on this document, including this Copyright Notice, License and Disclaimer. The Connectivity Standards Alliance does not grant you any license hereunder other than as expressly stated herein.
</p>

<p>
  Elements of this document may be subject to third party intellectual property rights, including without limitation, patent, copyright or trademark rights, and any such third party may or may not be a member of the Connectivity Standards Alliance. Connectivity Standards Alliance members grant other Connectivity Standards Alliance members certain intellectual property rights as set forth in the Connectivity Standards Alliance IPR Policy. Connectivity Standards Alliance members do not grant you any rights under this license. The Connectivity Standards Alliance is not responsible for, and shall not be held responsible in any manner for, identifying or failing to identify any or all such third party intellectual property rights. Please visit www.csa-iot.org for more information on how to become a member of the Connectivity Standards Alliance.
</p>

<p>
  This document and the information contained herein are provided on an “AS IS” basis and the Connectivity Standards Alliance DISCLAIMS ALL WARRANTIES EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO (A) ANY WARRANTY THAT THE USE OF THE INFORMATION HEREIN WILL NOT INFRINGE ANY RIGHTS OF THIRD PARTIES (INCLUDING WITHOUT LIMITATION ANY INTELLECTUAL PROPERTY RIGHTS INCLUDING PATENT, COPYRIGHT OR TRADEMARK RIGHTS); OR (B) ANY IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, TITLE OR NONINFRINGEMENT. IN NO EVENT WILL THE CONNECTIVITY STANDARDS ALLIANCE BE LIABLE FOR ANY LOSS OF PROFITS, LOSS OF BUSINESS, LOSS OF USE OF DATA, INTERRUPTION OF BUSINESS, OR FOR ANY OTHER DIRECT, INDIRECT, SPECIAL OR EXEMPLARY, INCIDENTIAL, PUNITIVE OR CONSEQUENTIAL DAMAGES OF ANY KIND, IN CONTRACT OR IN TORT, IN CONNECTION WITH THIS DOCUMENT OR THE INFORMATION CONTAINED HEREIN, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH LOSS OR DAMAGE.
</p>

<p>
  All company, brand and product names in this document may be trademarks that are the sole property of their respective owners.
</p>

<p>
  This notice and disclaimer must be included on all copies of this document.
</p>

<p>
  Connectivity Standards Alliance<br>
  508 Second Street, Suite 206<br>
  Davis, CA 95616, USA<br>
</p>

# Participants

> PS：见原本

# Document Control

Matter Specification 由单独的章节组成，例如这一章。有关所有章节的列表，请参见第 1 章。章节之间的引用使用 *X.Y* 表示法，其中 X 是章节，Y 是该章节中的小节。对外部文件的引用包含在第 1 章中，并使用 *\[Rn\]* 表示法。对这些章节中任何一章的更新都将反映在对下面源文档列表的更新中。

* Chapter 01 — Introduction Document # \[./Ch01_Introduction.adoc\]
* Chapter 02 — Architecture Document # \[./Ch02_Architecture.adoc\]
* Chapter 03 — Cryptographic Primitives Document # \[./Ch03_Cryptography.adoc\]
* Chapter 04 — Secure Channel Document # \[./Ch04_Secure_Channel.adoc\]
* Chapter 05 — Commissioning Document # \[./Ch05_Commissioning.adoc\]
* Chapter 06 — Device Attestation Document # \[./Ch06_Attestation.adoc\]
* Chapter 07 — Data Model Document # \[./Ch07_Data_Model.adoc\]
* Chapter 08 — Interaction Model Document # \[./Ch08_Interaction_Model.adoc\]
* Chapter 09 — System Model Document # \[./Ch09_System_Model.adoc\]
* Chapter 10 — Interaction Encoding Document # \[./Ch10_Interaction_Encoding.adoc\]
* Chapter 11 — Device Management Document # \[./Ch07_Management.adoc\]
* Chapter 12 — Multiple Fabrics Document # \[./Ch09_MultipleAdmins.adoc\]
* Chapter 13 — Security Requirements Document # \[./Ch10_Security_Requirements.adoc\]

# Revision History

| Revision | Date               | Details       | Editor          |
| :------- | :----------------- | :------------ | :-------------- |
| 01       | May 11, 2020       | Initial draft | Robert Szewczyk |
| 02       | September 23, 2022 | Version 1.0   | Robert Szewczyk |

# Table of Contents

- [x] [Copyright Notice, License and Disclaimer](#copyright-notice-license-and-disclaimer)
- [x] [Participants](#participants)
- [x] [Document Control](#document-control)
- [x] [Revision History](#revision-history)
- [x] [Chapter 1. Introduction](chapter-01.md#chapter-1-introduction)
  - [x] [1.1. Scope and Purpose](chapter-01.md#11-scope-and-purpose)
  - [x] [1.2. Acronyms and Abbreviations](chapter-01.md#12-acronyms-and-abbreviations)
  - [x] [1.3. Definitions](chapter-01.md#13-definitions)
  - [x] [1.4. Standards Terminology Mapping](chapter-01.md#14-standards-terminology-mapping)
  - [x] [1.5. Conformance Levels](chapter-01.md#15-conformance-levels)
  - [x] [1.6. References](chapter-01.md#16-references)
    - [x] [1.6.1. CSA Reference Documents](chapter-01.md#161-csa-reference-documents)
    - [x] [1.6.2. External Reference Documents](chapter-01.md#162-external-reference-documents)
  - [x] [1.7. Informative References](chapter-01.md#17-informative-references)
    - [x] [1.7.1. CSA Reference Documents](chapter-01.md#171-csa-reference-documents)
  - [x] [1.8. Conventions](chapter-01.md#18-conventions)
    - [x] [1.8.1. Enumerations and Reserved Values](chapter-01.md#181-enumerations-and-reserved-values)
    - [x] [1.8.2. Reserved Bit Fields](chapter-01.md#182-reserved-bit-fields)
    - [x] [1.8.3. Number Format](chapter-01.md#183-number-format)
    - [x] [1.8.4. Provisional](chapter-01.md#184-provisional)
