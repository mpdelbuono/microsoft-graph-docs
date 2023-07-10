---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new HorizontalSection();
$requestBody->setEmphasis(new SectionEmphasisType('strong'));

$requestBody->setLayout(new HorizontalSectionLayoutType('twoColumns'));



$result = $graphServiceClient->sites()->bySiteId('site-id')->pages()->bySitePageId('sitePage-id')->canvasLayout()->horizontalSections()->byHorizontalSectionId('horizontalSection-id')->patch($requestBody);


```