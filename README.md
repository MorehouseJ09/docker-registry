Jumper Docker Registry (fork from dotcloud/docker-registry)
=

Overview
-

-	1.) Docker registry for jumper application built on dotcloud 
-	2.) Should use s3 bucket (jumper-docker-images) for backup
-	3.) Nginx application with private authentication for internal use only

Directions
-

-	push the application live

	`dotcloud create docker && dotcloud push`

-	Link the custom domain (docker.jumperapi.com) to the dotcloud app 

	`dotcloud domain add api docker.jumperapi.com`

-	Update route53 zone records for domain. CNAME = gateway.dotcloud.com

Test
-

-	docker tag imageId tagName
-	docker commit tagName

