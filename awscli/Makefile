#
# Makefile for awscli
#
usage:
	@echo "usage: make [install|test|version]"

install-aws1:
	brew install awscli

install-aws2:
	curl "https://d1vvhvl2y92vvt.cloudfront.net/awscli-exe-macos.zip" -o "awscliv2.zip"
	unzip awscliv2.zip
	sudo ./aws/install

config:
	aws configure
	#aws configure set default.s3.signature_version s3v4

test t:
	aws s3 ls
	#aws s3 cp myvideo.mp4 s3://mybucket/
	aws2 s3 ls
	#aws --endpoint-url https://play.min.io:9000 s3 ls

version:
	aws --version
	#aws-cli/1.16.310 Python/3.7.6 Darwin/19.2.0 botocore/1.13.46
	aws2 --version
	#aws-cli/2.0.0dev3 Python/3.7.4 Darwin/19.2.0 botocore/2.0.0dev2

verify:
	curl -o awscliv2.sig https://d1vvhvl2y92vvt.cloudfront.net/awscli-exe-macos.zip.sig
	gpg --verify awscliv2.sig awscliv2.zip

git-update gu:
	cd ..; make gu

