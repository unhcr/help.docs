# Deploying help.unhcr.org

The deploy process for help.unhcr.org is meant to be as simple as possible. For the most part this is the case. To manage deploy, help.unhcr.org uses [wp-cli-deploy](https://github.com/c10b10/wp-cli-deploy).

Follow the instructions on the github page to install `wp-cli-deploy`. You can read those docs as well to understand all the variables in the `wp-config.php` file.

In sum you can use these commands to push to the production server:

Pushes all themes to the production server
`wp deploy push prod --what=themes`

Pushes all uploads to the production server
`wp deploy push prod --what=uploads`

There is also an option to push the database, but due to security reasons this is not enabled since it requires the ability to connect on the mysql port to the production server.

To push the database, which you shouldn't have to do often, run a `mysqldump` on the wordpress database and then use scp to transfer the file to the production server. Finally upload the mysqldump to the production database.

There also exists a staging server that's only accessible within the UNHCR network. For this, you can use the same commands as above except use `staging` instead of `prod`:

Pushes all themes to the staging server
`wp deploy push staging --what=themes`

Pushes all uploads to the staging server
`wp deploy push staging --what=uploads`

For staging, we do not have to worry about the security issues since it's only accessible via the UNHCR network you can easily push the local database with this command:

`wp deploy push staging --what=db`

