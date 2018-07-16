# ScaleIT Black Cylinder App

The ScaleIT Black Cylinder App is just a ScaleIT Demo App. It literally does nothing more than the ionic-app-skeleton.

## Usage

    git clone https://github.com/ScaleIT-Org/sapp-i40-app-skeleton.git My_New_ScaleiT_App
    
### With Git Submodule Composition

Add Node.js Domain Software:
    
    cd My_New_ScaleiT_App
    git submodule add https://github.com/ScaleIT-Org/nodejs-app-skeleton.git "Domain Software/MyNodejsApp"

Add a platform sidecar:

### File Based Composition/Copying

    mkdir MyNodejsApp
    git clone https://github.com/ScaleIT-Org/nodejs-app-skeleton.git MyNodejsApp
    
    # move or copy the Node.js skeleton to the Industry 4.0 Ready App Skeleton
    mv MyNodejsApp "My_New_ScaleiT_App/Domain Software"

    # optionally but recommended, remove the git version control from the Node.js skeleton
    cd "My_New_ScaleiT_App/Domain Software/MyNodejsApp"
    rm -rf .git

## Features
Contains 3 Folders to seperate the application components:

* Domain Software
  - contains the main app (Black Cylinder)
* Platform Sidecars
  - nothing, not needed by Black Cylinder
* Resources
  - Rancher (Documents for the Rancher catalog entry)

## How to build

Go to `Domain Software/Black Cylinder` and run
```
  docker-compose up -d --build
```

## Configuration

### Set Docker port

You can edit the published docker port by setting the property inside `docker-compose.yml`.

For example:
```
ports:
   - "8080:80"
```

## Notes

The `.gitkeep` files are just placeholders and can be deleted. This is due to the fact that git only checks in folders with files inside them.
