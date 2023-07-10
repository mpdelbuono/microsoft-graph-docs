---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SitePage();
$requestBody->setOdataType('#microsoft.graph.sitePage');

$requestBody->setTitle('sample');

$requestBody->setShowComments(true);

$requestBody->setShowRecommendedPages(false);



$result = $graphServiceClient->sites()->bySiteId('site-id')->pages()->bySitePageId('sitePage-id')->patch($requestBody);


```