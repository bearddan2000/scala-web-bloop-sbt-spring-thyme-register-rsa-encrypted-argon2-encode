# scala-web-bloop-sbt-spring-thyme-register-rsa-encrypted-argon2-encode

## Description
A springboot secure web app with thymeleaf support.
Three roles are defined; USER, ADMIN, and SUPER. All roles
can access pages `/home`, `/login`, and `/about`. Only USER
can access `/user` and ADMIN only `/admin` whereas SUPER can
navigate to either and have its own `/super`. Each role
has an action USER=VIEW ONLY, ADMIN=READ/WRITE, SUPER=CREATE.
All password are encrypted with RSA and encoded with argon2
to insure strong passwords.

The encrypted text is 512 in length when compressed ~ 306.
To compress the encrypted text gzip was used.

When storing a password it is best practice
to use a one-way hash such as bcrypt, scrypt,
or argon2.

Compiled and ran from build server `bloop`.

# Build note
Dependencies must be compatable with jdk8 or less.

## Tech stack
- bloop
- scala
- bloop-sbt

## Docker stack
- eed3si9n/sbt

## To run
`sudo ./install.sh -u`
Available at http://localhost
- Login with id: user and password: pass
- Login with id: admin and password: pass
- Login with id: super and password: pass

## To stop (optional)
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credits
- https://hellokoding.com/spring-security-login-logout-thymeleaf/
- https://www.javainterviewpoint.com/spring-security-inmemoryuserdetailsmanager/
