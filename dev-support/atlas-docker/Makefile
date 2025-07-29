SOLR_VERSION=8

atlas-solr:
	docker buildx build \
		-t hub.hmf.xyz/emr/atlas-solr:${SOLR_VERSION} \
		--platform linux/amd64 \
		-f Dockerfile.atlas-solr .
	docker push hub.hmf.xyz/emr/atlas-solr:${SOLR_VERSION}