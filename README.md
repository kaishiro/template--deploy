```
git clone https://github.com/kaishiro/template-deploy.git deploy

rm -rf .git

git init

git config user.name "Matthew White"

git config user.email "matt@substructu.re"

# Add any config vars to env.rb

# Modify clone URL in deploy

git add .

git commit -m "Initial Commit"

heroku apps:create DEPLOY-NAMESPACE

git push heroku master

heroku addons:add scheduler

heroku addons:open scheduler

# Enter 'sh deploy' into scheduler task field, set interval to compile every 10 minutes
```
