---
title: "Tuáº§n 2 - XÃ¢y ná»n táº£ng backend vÃ  xÃ¡c thá»±c"
date: 2026-06-22
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Má»¥c tiÃªu

- HoÃ n thiá»‡n backend skeleton vá»›i FastAPI, SQLAlchemy vÃ  migration.
- XÃ¢y luá»“ng Ä‘Äƒng kÃ½, Ä‘Äƒng nháº­p vÃ  phÃ¢n quyá»n theo ba vai trÃ².
- Chuáº©n bá»‹ database PostgreSQL cho mÃ´i trÆ°á»ng AWS.

### CÃ´ng viá»‡c Ä‘Ã£ thá»±c hiá»‡n

| Thá»© | CÃ´ng viá»‡c | NgÃ y báº¯t Ä‘áº§u | NgÃ y hoÃ n thÃ nh | TÃ i liá»‡u |
| --- | --- | --- | --- | --- |
| Thá»© 2 | Khá»Ÿi táº¡o FastAPI app, cáº¥u hÃ¬nh settings, dependency injection vÃ  module router. | 22/06/2026 | 22/06/2026 | [FastAPI - Bigger Applications](https://fastapi.tiangolo.com/tutorial/bigger-applications/), [FastAPI Project Generation](https://fastapi.tiangolo.com/project-generation/) |
| Thá»© 3 | Táº¡o schema users, role enum, password hashing vÃ  JWT authentication. | 23/06/2026 | 23/06/2026 | [FastAPI - OAuth2 with JWT](https://fastapi.tiangolo.com/tutorial/security/oauth2-jwt/) |
| Thá»© 4 | Viáº¿t API Ä‘Äƒng kÃ½ cho á»©ng viÃªn vÃ  doanh nghiá»‡p, Ä‘á»“ng thá»i seed tÃ i khoáº£n quáº£n trá»‹ viÃªn an toÃ n. | 24/06/2026 | 24/06/2026 | [OpenAPI Specification](https://swagger.io/specification/) |
| Thá»© 5 | Táº¡o migration Ä‘áº§u tiÃªn cho PostgreSQL vÃ  kiá»ƒm tra tÃ­nh tÆ°Æ¡ng thÃ­ch vá»›i Amazon RDS. | 25/06/2026 | 25/06/2026 | [Alembic Documentation](https://alembic.sqlalchemy.org/en/latest/), [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html) |
| Thá»© 6 | Thiáº¿t láº­p IAM policy vÃ  parameter placeholder cho secrets káº¿t ná»‘i database trÃªn AWS. | 26/06/2026 | 26/06/2026 | [AWS IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html), [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) |
| Thá»© 7 | Kiá»ƒm thá»­ Ä‘Äƒng nháº­p nhiá»u vai trÃ² vÃ  xá»­ lÃ½ cÃ¡c lá»—i 401, 403, validation. | 27/06/2026 | 27/06/2026 | [FastAPI Testing](https://fastapi.tiangolo.com/tutorial/testing/), [Postman API Testing](https://learning.postman.com/docs/tests-and-scripts/write-scripts/test-scripts/) |

### Káº¿t quáº£ Ä‘áº¡t Ä‘Æ°á»£c

- Backend ná»n táº£ng Ä‘Ã£ á»•n Ä‘á»‹nh, há»— trá»£ phÃ¢n quyá»n vÃ  sáºµn sÃ ng má»Ÿ rá»™ng nghiá»‡p vá»¥ tuyá»ƒn dá»¥ng.
- Thiáº¿t káº¿ dá»¯ liá»‡u phÃ¹ há»£p Ä‘á»ƒ triá»ƒn khai lÃªn Amazon RDS mÃ  khÃ´ng phá»¥ thuá»™c mÃ´i trÆ°á»ng local.


