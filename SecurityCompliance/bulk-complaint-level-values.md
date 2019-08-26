---
title: "Bulk Complaint Level values, bulk mailers, BCL levels, how BCL works, BCL ratings, Antispam, Antispam header, bulk mail filtering, stop bulk mail"
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 8/23/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
ms.collection:
- M365-security-compliance
description: "Bulk mailers vary in their sending patterns, content creation, and list acquisition practices. Some are good bulk mailers that send wanted messages with relevant content to their subscribers. These messages generate few complaints from recipients. Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients. To distinguish these types of bulk mailers, messages from bulk mailers are assigned a Bulk Complaint Level (BCL) rating. BCL ratings range from 1 to 9 depending on how likely the bulk mailer is to generate complaints. A sender that has a rating of BCL 9 is likely to generate many complaints from recipients, whereas a rating of BCL 3 is unlikely to generate many complaints. Microsoft uses both internal and third-party sources to identify bulk mail and determine the appropriate BCL. This rating is exposed in the X-Microsoft-Antispam header of every message. For more information about this message header, see Anti-spam message headers."
---

# Bulk Complaint Level values

Bulk mailers vary in their sending patterns, content creation, and list acquisition practices. Some are good bulk mailers that send wanted messages with relevant content to their subscribers. These messages generate few complaints from recipients. Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients. To distinguish these types of bulk mailers, messages from bulk mailers are assigned a Bulk Complaint Level (BCL) rating. BCL ratings range from 1 to 9 depending on how likely the bulk mailer is to generate complaints. A sender that has a rating of BCL 9 is likely to generate many complaints from recipients, whereas a rating of BCL 3 is unlikely to generate many complaints. Microsoft uses both internal and third-party sources to identify bulk mail and determine the appropriate BCL. This rating is exposed in the **X-Microsoft-Antispam** header of every message. For more information about this message header, see [Anti-spam message headers](anti-spam-message-headers.md).

Since a bulk mailer with a rating of 9 is likely to generate complaints, the default BCL is 7. This means that bulk mails will be accepted until the complaint level of 7 and mail won't be accepted thereafter. The lower the rating, the less bulk mail is accepted. If your users are, and their work is, sensitive to bulk mail, and your BCL is set to 4, then no bulk mail with a higher BCL than 4 will be accepted.
  
You can use BCL values to set the desired level of bulk filtering your organization requires by following the steps in [Configure your spam filter policies](configure-your-spam-filter-policies.md).
  
More BCL values are being added and will be included here in the future. The following table lists and describes the BCL values that are currently in use.
  
|||
|:-----|:-----|
|**BCL Value** <br/> |**Description** <br/> |
|0  <br/> |The message isn't from a bulk sender.  <br/> |
|1, 2, 3  <br/> |The message is from a bulk sender that generates few complaints.  <br/> |
|4, 5, 6, 7  <br/> |The message is from a bulk sender that generates a mixed number of complaints.  <br/> |
|8, 9  <br/> |The message is from a bulk sender that generates a high number of complaints  <br/> |
   

