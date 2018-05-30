This is a sample to use external config with spring boot.

If you are running the jar command in the same path of the jar, you dont need specify the location.
The spring boot assumes the ./ and will look for "config" dir

> java -Dspring.profiles.active=other -jar propteste.jar

If you are in another path and are running the jar, will need specify the config location with full path.
It is valid for linux service execution too.
> java -Dspring.profiles.active=other -Dspring.config.location=file:"F:/jarpath/config/" -jar jarpath/propteste.jar

That jarpath its a single example, it can be any path
> java -Dspring.profiles.active=other -Dspring.config.location=file:"/home/myapp/config/" -jar jarpath/propteste.jar

You can even override an existing profile properties
> java -Dspring.profiles.active=qa -Dspring.config.location=file:"F:/jarpath/config/" -jar jarpath/propteste.jar
