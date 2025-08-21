SOLR_VERSION=8
CENTOS_VERSION=8
ATLAS_VERSION=2.4.0

atlas-solr:
	docker buildx build \
		-t hub.hmf.xyz/emr/atlas-solr:${SOLR_VERSION} \
		--platform linux/amd64 \
		-f Dockerfile.atlas-solr .
	docker push hub.hmf.xyz/emr/atlas-solr:${SOLR_VERSION}

atlas-base:
	docker buildx build \
		-t hub.hmf.xyz/emr/atlas-base:${ATLAS_VERSION} \
		--platform linux/amd64 \
		--build-arg CENTOS_VERSION=${CENTOS_VERSION} \
		-f Dockerfile.atlas-base .

atlas:
	docker buildx build \
		-t hub.hmf.xyz/emr/atlas:${ATLAS_VERSION} \
		--platform linux/amd64 \
		--build-arg ATLAS_VERSION=${ATLAS_VERSION} \
		-f Dockerfile.atlas .
	docker push hub.hmf.xyz/emr/atlas:${ATLAS_VERSION}