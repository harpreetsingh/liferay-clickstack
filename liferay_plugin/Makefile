compile: liferay.zip
	rm -f /tmp/cb_liferay.zip
# eventually needs to be an unzip
#	zip /tmp/cb_liferay.zip /tmp/liferay/*
	mv /tmp/liferay/liferay_with_tomcat.zip /tmp/liferay/cb_liferay.zip

# downloads liferay file; this will eventually be a bare boned liferay with TC and JDK
liferay.zip: 
#	the following should be download of liferay, followed by strip out of tomcat
	cp /Users/harpreet/liferay/liferay*.zip liferay_with_tomcat.zip
#	now reconstruct the bare-bones liferay (without tomcat and jdk)
	mkdir -p /tmp/liferay
	cp ./liferay_with_tomcat.zip /tmp/liferay/

# publishes the final liferay zip for use as CS
publish: compile
	s3cmd put /tmp/liferay/cb_liferay.zip -P s3://harpreet-clickstacks.cloudbees

clean:
	rm -rf /tmp/liferay/
	rm -f /tmp/cb_liferay.zip
