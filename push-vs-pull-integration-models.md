# Push vs Pull Integration models

## Conceptual

|No. | Concerns\Integration Model     | Push Model     | Pull Model     |  Hybrid Model     |
| --------------- | --------------- |:-----------|:-----------------|:-----------------|
|1. |  Governance - How certificate policy is enforced ? | Certificate policy **can be** enforced in a proactive or manual manner | Certificate policy **must be** enforced in a proactive manner. | Certificate policy **will be** enforced in a proactive manner through TPP Policy
|2. |  Governance - Visibility | Venafi's TPP | Venafi's TPP | Venafi's TPP |
|3. |  Governance - Reporting | Venafi's TPP | Venafi's TPP | Venafi's TPP |
|4. |  Governance - Notifications/Alerting | Venafi's TPP | Venafi's TPP **(and/or)** IaC Platform |Venafi's TPP |
|5. |  Governance - Management | Venafi's TPP | Venafi's TPP **(and/or)** IaC Platform |Venafi's TPP |
|6. |  Increasing footprint of certificate endpoints (Cloud/DevOps/NetOps) | Not Recommended | Recommended | Recommended
|7. |  How to integrate with change management process (SNOW) ? | Venafi's TPP | Venafi's TPP **(and/or)** IaC Platform | Venafi's TPP 
|8. |  What manages certificate lifecycle process ? | Venafi's TPP | Venafi's TPP **(and)** IaC Platform | Venafi's TPP (auto-renewal & auto-provision) |
|9. |  Ephemeral infrastructure and application deployment (Dynamic environment) | Not Recommended | Recommended | Recommended |
|10. |  Non ephemeral infrastructure and ephemeral application deployment | Recommended | Recommended |  
|11. |  Non Ephemeral infrastructure and application deployment (Static environment) | Recommended | Not Recommended | Recommened  |
|12. |  State management | Venafi's TPP | IaC platforms |Venafi's TPP |
|13. |  Which model provides ease of Integratation with exiting CI/CD pipelines/workflows ? | Intermediate| Easy | Easy/Intermediate | 
|14. |  Certificate Ownership (InfoSec/Security Engineering team) | Recommended | Not Recommended |  
|15. |  Certificate Ownership (Platforms) | Recommended | Recommended |
|16. |  Certificate Ownership (Development & Deployment Team) | Recommended (only for smaller/manual environments) | Recommended | Recommended 

<br>

## Technical 

|No. | Concerns\Integration Model     | Push Model     | Pull Model     |
| --------------- | --------------- |:-----------|:-----------------|
|1. |  Request/Renew cerificate | Venafi's TPP | IaC platform |IaC platform through TPP
|2. |  Request/Renew + Install certificate | Venafi's TPP | IaC platforms | IaC platform through TPP
|3. |  Decommission certificate | Venafi's TPP | IaC platforms **(and)** Venafi's TPP | IaC platform through TPP
|4. |  Private/Public key generation | Venafi's TPP | IaC platforms || Venafi TPP
|5. |  Organization in TPP | Folders/Device/Application/Certificate/Custom Fields | Folders/Certificate/Custom Fields | Folders/Device/Application/Certificate/
|6. |  Validation/Monitoring | Venafi's TPP | IaC platform **(and/or)** Venafi's TPP (certificate based) |Venafi's TPP |
|7. |  Notifications | Venafi's TPP | IaC platform **(and/or)** Venafi's TPP | Venafi's TPP |
|8. |  Private Key Location | Venafi's TPP | IaC platforms | Venafi's TPP 
|9. |  Automated Renewals | Venafi's TPP | IaC platforms |  Venafi's TPP 

<br>
![image](https://user-images.githubusercontent.com/94073641/150851761-03367d86-2555-45d4-816b-87a785bac950.png)

|No. | Concerns\Integration Model     | Push Model     | Pull Model     |  Hybrid Model     |
| --------------- | --------------- |:-----------|:-----------------|:-----------------|
|1. |  Governance - How certificate policy is enforced ? | Certificate policy **can be** enforced in a proactive or manual manner | Certificate policy **must be** enforced in a proactive manner. | Certificate policy **will be** enforced in a proactive manner through TPP Policy
|2. |  Governance - Visibility | Venafi's TPP | Venafi's TPP | Venafi's TPP |
|3. |  Governance - Reporting | Venafi's TPP | Venafi's TPP | Venafi's TPP |
|4. |  Governance - Notifications/Alerting | Venafi's TPP | Venafi's TPP **(and/or)** IaC Platform |Venafi's TPP |
|5. |  Governance - Management | Venafi's TPP | Venafi's TPP **(and/or)** IaC Platform |Venafi's TPP |
|6. |  Increasing footprint of certificate endpoints (Cloud/DevOps/NetOps) | Not Recommended | Recommended | Recommended
|7. |  How to integrate with change management process (SNOW) ? | Venafi's TPP | Venafi's TPP **(and/or)** IaC Platform | Venafi's TPP 
|8. |  What manages certificate lifecycle process ? | Venafi's TPP | Venafi's TPP **(and)** IaC Platform | Venafi's TPP (auto-renewal & auto-provision) |
|9. |  Ephemeral infrastructure and application deployment (Dynamic environment) | Not Recommended | Recommended | Recommended |
|10. |  Non ephemeral infrastructure and ephemeral application deployment | Recommended | Recommended |  
|11. |  Non Ephemeral infrastructure and application deployment (Static environment) | Recommended | Not Recommended | Recommened  |
|12. |  State management | Venafi's TPP | IaC platforms |Venafi's TPP |
|13. |  Which model provides ease of Integratation with exiting CI/CD pipelines/workflows ? | Intermediate| Easy | Easy/Intermediate | 
|14. |  Certificate Ownership (InfoSec/Security Engineering team) | Recommended | Not Recommended |  
|15. |  Certificate Ownership (Platforms) | Recommended | Recommended |
|16. |  Certificate Ownership (Development & Deployment Team) | Recommended (only for smaller/manual environments) | Recommended | Recommended 

<br>

## Technical 

|No. | Concerns\Integration Model     | Push Model     | Pull Model     |
| --------------- | --------------- |:-----------|:-----------------|
|1. |  Request/Renew cerificate | Venafi's TPP | IaC platform |IaC platform through TPP
|2. |  Request/Renew + Install certificate | Venafi's TPP | IaC platforms | IaC platform through TPP
|3. |  Decommission certificate | Venafi's TPP | IaC platforms **(and)** Venafi's TPP | IaC platform through TPP
|4. |  Private/Public key generation | Venafi's TPP | IaC platforms || Venafi TPP
|5. |  Organization in TPP | Folders/Device/Application/Certificate/Custom Fields | Folders/Certificate/Custom Fields | Folders/Device/Application/Certificate/
|6. |  Validation/Monitoring | Venafi's TPP | IaC platform **(and/or)** Venafi's TPP (certificate based) |Venafi's TPP |
|7. |  Notifications | Venafi's TPP | IaC platform **(and/or)** Venafi's TPP | Venafi's TPP |
|8. |  Private Key Location | Venafi's TPP | IaC platforms | Venafi's TPP 
|9. |  Automated Renewals | Venafi's TPP | IaC platforms |  Venafi's TPP 

<br>
![image](https://user-images.githubusercontent.com/94073641/150851762-ce5f86f8-9611-40af-90c0-ee219cfc108f.png)
