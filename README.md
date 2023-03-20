# Tech Blog Seeding App

This is a seeding application for challenge 14, tech blog app, for the Edx full stack program. 

## How to Use

Install fakerjs
````
npm i @faker-js/faker
````

Put seed.js and createSeeds.js in a seeds folder for challenge 14. 
Add the script to the package.json
````
"seed": "node seeds/seed.js"
````
Start by updating the createSeeds.js so that the properties match your own models. 

Your post content needs to be DataTypes.TEXT to hold long posts. You may want to do the same to the comment body and control its length with the seed code.

Add date_created to both Comment and Post model so that your create dates can be randomized. If you fall back on the Sequelize timestamp createdAt, all the dates will be the date you ran the seed program. If that's ok with you then comment out the date_created properties in createSeeds.js

In the createSeeds.js you may make any changes to the seeds that you want. If you want more users, increase the Array length, if you want different date ranges, you can adjust that as well, anything you want can be changed.

Run the createSeeds.js
````
node seeds/createSeeds.js
````

If you want to add some easy to remember user accounts, do that now in the user_data.json file.

Run the seed program
````
npm run seed
````

### Heroku/Jaws

To seed on heroku please install the Heroku CLI. You can enter the bash command line like this:
````
heroku run bash -a app-name
````
Then run your script again. The same data seeded on localhost will be seeded to the JawsDB when you run
````
npm run seed
````
unless you choose to run the createSeeds.js again.

You can use this program for project 2 as well - just change the createSeeds code as needed for your models. 

## Credits

FakerJS https://fakerjs.dev/api/


## Questions

Email me directly at my bootcamp spot email or Slack me if you are in my cohort. 