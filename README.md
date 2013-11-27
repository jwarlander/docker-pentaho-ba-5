Pentaho Business Analytics 5.0
==============================

Simple setup for running Pentaho Business Analytics (Community Edition) in evaluation mode; eg. the default evaluation user accounts are still in place. No extras included.

## Getting Started ##

Start a container with forwarding of port 8080 from the host:

    CONTAINER_ID=`docker run -d -p 8080:8080 jwarlander/pentaho-ba-5`

Watch the output and wait for the server to start up completely:

    docker attach -nostdin -sig-proxy=false $CONTAINER_ID

You'll want to see some lines like the following, after about 40-300 seconds depending on your host performance characteristics:

    ...<other output>...
    Pentaho BI Platform server is ready. (Pentaho Platform Core 5.0.1-stable.-1) Fully Qualified Server Url = http://localhost:8080/pentaho/, Solution Path = /opt/pentaho/biserver-ce/pentaho-solutions
    Nov 27, 2013 12:56:25 PM org.apache.catalina.startup.HostConfig deployDirectory
    INFO: Deploying web application directory ROOT
    Nov 27, 2013 12:56:25 PM org.apache.coyote.http11.Http11Protocol start
    INFO: Starting Coyote HTTP/1.1 on http-8080
    Nov 27, 2013 12:56:26 PM org.apache.jk.common.ChannelSocket init
    INFO: JK: ajp13 listening on /0.0.0.0:8009
    Nov 27, 2013 12:56:26 PM org.apache.jk.server.JkMain start
    INFO: Jk running ID=0 time=0/1228  config=null
    Nov 27, 2013 12:56:26 PM org.apache.catalina.startup.Catalina start
    INFO: Server startup in 287987 ms

Connect to http://localhost:8080/ and wait for the Pentaho User Console login page to display. Click on "Login as Evaluator" to see your options.
