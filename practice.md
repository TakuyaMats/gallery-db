# Gallery Database

## DEPENDENCIES / NPM PACKAGES
-dotenv
-express
-express-handlebars
-handlebars
-mysql2
-sequelize

## IMPORTANT
-make sure to setup mysql workbench and DB/config folder with database connection and schema.sql


## Models

### Gallery
ID (primary key)
NAME-string
starting_date DATE
ending_date DATE

### Painting
ID (primary key)
title String
artist String
exhibition_date DATE
filename STRING
description STRING
gallery_id INT references gallery

### User
ID (primary key)
username STRING
email STRING, unique true validate
passowrd STRING validate length

## ASSOCIATIONS
set up associations between gallery and painting make sure to include foreign key

## SEEDS

### GalleryData 
const gallerydata = [
  {
    name: 'Printemps',
    starting_date: 'April 20, 2021 07:00:00',
    ending_date: 'June 21, 2021 17:00:00',
  },
  {
    name: 'Sommer',
    starting_date: 'June 22, 2021 09:00:00',
    ending_date: 'September 22, 2021 22:00:00',
  },
  {
    name: 'Herfst',
    starting_date: 'September 23, 2021 08:30:00',
    ending_date: 'December 21, 2021 20:30:00',
  },
  {
    name: 'Invierno',
    starting_date: 'December 22, 2020 11:00:00',
    ending_date: 'March 19, 2021 19:00:00',
  },
];

### Painting Data

const paintingdata = [
  {
    title: 'Blossoming Apricot',
    artist: 'LedyX',
    exhibition_date: 'March 30, 2018',
    gallery_id: 1,
    filename: '01-blossoming-apricot.jpg',
    description:
      'Branches with pink apricot blossoms against a blue background.',
  },
  {
    title: 'Cosmos Flowers',
    artist: 'WStudio',
    exhibition_date: 'May 05, 2017',
    gallery_id: 1,
    filename: '02-cosmos-flowers.jpg',
    description: 'Pink cosmos flowers against a blue sky.',
  },
  {
    title: 'Sand + Sea = Summer',
    artist: 'S_Photo',
    exhibition_date: 'June 10, 2019',
    gallery_id: 2,
    filename: '03-sand-sea-summer.jpg',
    description: 'Sandy beach with the blue sea and sky in the background.',
  },
  {
    title: 'Beach Chairs',
    artist: 'icemanphotos',
    exhibition_date: 'July 4, 2020',
    gallery_id: 2,
    filename: '04-beach-chairs.jpg',
    description: 'Two beach chairs under a beach umbrella on the beach.',
  },
  {
    title: 'Beach Sunrise',
    artist: 'VRstudio',
    exhibition_date: 'August 14, 2016',
    gallery_id: 2,
    filename: '05-beach-sunrise.jpg',
    description: 'Sun setting in the horizon with waves lapping the shore.',
  },
  {
    title: 'Fall Colors',
    artist: 'DrivingJack',
    exhibition_date: 'October 15, 2018',
    gallery_id: 3,
    filename: '06-fall-colors.jpg',
    description:
      'Trees with red, orange, yellow leaves reflected on a still lake.',
  },
  {
    title: 'Autumn Mountains',
    artist: 'Vitalii_Mamchuk',
    exhibition_date: 'November 3, 2016',
    gallery_id: 3,
    filename: '07-autumn-mountains.jpg',
    description:
      'Mountains with red and yellow leaves against a background of hazy rolling hills.',
  },
  {
    title: 'Frozen River',
    artist: 'Vlad Sokolovsky',
    exhibition_date: 'December 24, 2020',
    gallery_id: 4,
    filename: '08-frozen-river.jpg',
    description:
      'Trees with white frozen branches reflected on a frozen river against a light pink sky.',
  },
  {
    title: 'Winter Home',
    artist: 'Smit',
    exhibition_date: 'January 20, 2018',
    gallery_id: 4,
    filename: '09-winter-home.jpg',
    description:
      'Log cabin blanketed in heavy white snow with tall snow covered pine trees in the background.',
  },
];

-be sure to use bulkCreate 




