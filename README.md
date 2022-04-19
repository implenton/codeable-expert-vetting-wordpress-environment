# WordPress environment for vetting Codeable experts

👉 [Read the article](https://www.implenton.com/my-wordpress-environment-for-vetting-codeable-experts/) 👈

## Super short version

Run the `setup` script:

```shell
chmod +x ./setup
./setup
```

Then clone the applicant's CodeScreen repository into the environment:

```shell
git clone git@github.com:codescreen/CodeScreen_xxx.git
```

Map the plugin or theme into the WordPress instance by editing the `.wp-env.json` file:

```json
{
    "mappings": {
        "wp-content/plugins/xxx": "./CodeScreen_xxx/wp-content/plugins/xxx"
    }
}
```

Start, stop and destroy the envinroment with:

```shell
npx wp-env start
npx wp-env stop
npx wp-env destroy
```

For PHPCS, run:

```shell
./phpcs ./CodeScreen_xxx/wp-content/plugins/xxx
```
