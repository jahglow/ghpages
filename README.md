# ghpages
Tool to create a github page for Polymer seed element (modified from [Polymer Reusable Elment](https://www.polymer-project.org/1.0/docs/start/reusableelements.html#publishing-a-demo-and-landing-page-for-your-element) )

Once the demo and the docs look good locally, make sure that you’ve pushed any changes to your repo’s master branch. Also, make sure that you’ve updated the name and paths throughout your project, including the ones in `bower.json`. You shouldn’t have any remaining references to seed-element.

You can now use the `gp.sh` script to push a landing page for your element to GitHub pages. Inside your terminal, walk through running the following commands.

###Important: 
Make sure you run the gp.sh script in a temporary directory, as described below. The script overwrites the contents of the current directory.

    
    # Navigate back to your development directory
    cd ..
    
    ### git clone the Polymer tools repository
    git clone git://github.com/jahglow/ghpages.git
    
    ### Create a temporary directory for publishing your element and cd into it
    mkdir temp && cd temp
    
    # Run the gp.sh script. This will allow you to push a demo-friendly
    # version of your page and its dependencies to a GitHub pages branch
    # of your repository (gh-pages). Below, we pass in a GitHub username
    # and the repo name for our element
    "..\tools\gp.sh" gitHubUserName element-name
    
    # Finally, delete your temporary directory as you no longer require it


This will create a new gh-pages branch (or clone and clear the current one) then push a shareable version of your element to it. To see your newly-published docs, point a browser at:

    http://gitHubUserName.github.io/element-name/
