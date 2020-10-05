## Npm-package
# How to create a npm package?

# HERE IS YOUR ANSWER.

##If you are using npmrc to manage accounts on multiple registries, on the command line, switch to the appropriate profile:
 npmrc <profile-name>
On the command line, create a directory for your package:
 mkdir my-test-package
Navigate to the root directory of your package:
 cd my-test-package
If you are using git to manage your package code, in the package root directory, run the following commands, replacing git-remote-url with the git remote URL for your package:
 git init
 git remote add origin git://git-remote-url
In the package root directory, run the npm init command and pass the scope to the scope flag:
For an Org-scoped package, replace my-org with the name of your Org:
 npm init --scope=@my-org
For a user-scoped package, replace my-username with your username:
 npm init --scope=@my-username
Respond to the prompts to generate a package.json file. For help naming your package, see “Package name guidelines”.
Create a README file that explains what your package code is and how to use it.
In your preferred text editor, write the code for your package.
Reviewing package contents for sensitive or unnecessary information§
Publishing sensitive information to the registry can harm your users, compromise your development infrastructure, be expensive to fix, and put you at risk of legal action. We strongly recommend removing sensitive information, such as private keys, passwords, [personally identifiable information][pii] (PII), and credit card data before publishing your package to the registry. Even if your package is private, sensitive information can be exposed if the package is made public or downloaded to a computer that can be accessed by more users than intended.

For less sensitive information, such as testing data, use a .npmignore or .gitignore file to prevent publishing to the registry. For more information, see this article.

Testing your package§
To reduce the chances of publishing bugs, we recommend testing your package before publishing it to the npm registry. To test your package, run npm install with the full path to your package directory:

npm install my-package
Publishing private packages§
By default, scoped packages are published with private visibility.

On the command line, navigate to the root directory of your package.
cd /path/to/package
To publish your private package to the npm registry, run:
npm publish
To see your private package page, visit https://npmjs.com/package/package-name, replacing package-name with the name of your package. Private packages will say private below the package name on the npm website.
private package page showing private below package name

For more information on the publish command, see the CLI documentation.

< Creating and publishing scoped public packages | Package name guidelines >
The current stable version of npm is here. To upgrade, run: npm install npm@latest -g
