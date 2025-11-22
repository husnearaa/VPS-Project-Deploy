# VPS Project Deploy

## Step-1

First enter VPS IP address

```js
sss root@<ip address>
```

Then enter your password

```js
root@<ip address>'s password:
```

## Step-2

Go to www folder

```js
cd /var/www
```

Check all the project list

```js
ls;
```

## Step-3

Clone your github project ( have to clone the SSH file )

```js
git clone (the SSH link)
example: git clone git@github.com:husnearaa/VPS-Project-Deploy.git
```

## Step-4

```js
ls;
```

```js
cd vps-project-deploy/
```

```js
npm i
```

```js
npm run build
```

## Step-5

```js
sudo ufw enable
```

```js
sudo ufw status
```

```js
sudo ufw allow 5008
```

```js
sudo ufw status
```

```js
npm run start
```

```js
sudo ufw reload
```

## Step-6

```js
npm i -g pm2
```

```js
pm2 start npm --name "vps-project-deploy" -- start
```

```js
pm2 logs vps-project-deploy
```

```js
pm2 ls
```


# After Successfully Deploy — For Redeploy, Follow These Steps

```bash
git pull
```
Fetch and merge the latest code updates from GitHub.

```bash
npm i
```
Reinstall dependencies if there are any new changes.

```bash
npm run build
```
Rebuild your project to apply the new code changes.

```bash
pm2 ls
```
Check your PM2 process list to find the app ID.

```bash
pm2 restart <id_no>
```
Restart your specific app using its PM2 ID to apply the latest version.