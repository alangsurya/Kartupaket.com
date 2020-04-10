# Hallo Gays

Selamat Pagi Gays Ku....


https://www.kartupaket.com/?m=1
<a href="https://www.kartupaket.com/2020/03/cara-beli-kartu-byu-telkomsel-kartu.html?m=1">Baca Disini</a>

English 
Search topics, products...
GitHub.com GitHub Pages Configuring a custom domain for your GitHub Pages site Managing a custom domain for your GitHub Pages site
Managing a custom domain for your GitHub Pages site
You can set up or update certain DNS records and your repository settings to point the default domain for your GitHub Pages site to a custom domain.

Mac
Windows
Linux
GitHub Pages is available in public repositories with GitHub Free, and in public and private repositories with GitHub Pro, GitHub Team, GitHub Enterprise Cloud, and GitHub Enterprise Server. For more information, see "GitHub's products."

In this article
About custom domain configuration
Configuring a subdomain
Configuring an apex domain
Further reading
People with admin permissions for a repository can configure a custom domain for a GitHub Pages site.

About custom domain configuration
Make sure you add your custom domain to your GitHub Pages site before configuring your custom domain with your DNS provider. Configuring your custom domain with your DNS provider without adding your custom domain to GitHub could result in someone else being able to host a site on one of your subdomains.

Note: DNS changes can take up to 24 hours to propagate.

Configuring a subdomain
To set up a www or custom subdomain, such as www.example.com or blog.example.com, you must create a CNAME file in your site's repository and configure a CNAME record with your DNS provider.

On GitHub, navigate to your site's repository.
Under your repository name, click  Settings.
Repository settings button
Under "Custom domain", type your custom domain, then click Save. This will create a commit that adds a CNAME file in the root of your publishing source.
Save custom domain button
Navigate to your DNS provider and create a CNAME record that points your subdomain to the default domain for your site. For example, if you want to use the subdomain www.example.com for your user site, create a CNAME record that points www.example.com to <user>.github.io. For more information about how to create the correct record, see your DNS provider's documentation.For more information about the default domain for your site, see "About GitHub Pages."
Open Terminal.
To confirm that your DNS record configured correctly, use the dig command, replacing WWW.EXAMPLE.COM with your subdomain.
$ dig WWW.EXAMPLE.COM +nostats +nocomments +nocmd
  > ;WWW.EXAMPLE.COM.                     IN      A
  > WWW.EXAMPLE.COM.              3592    IN      CNAME   YOUR-USERNAME.github.io.
  > YOUR-USERNAME.github.io.      43192   IN      CNAME    GITHUB-PAGES-SERVER .
  >  GITHUB-PAGES-SERVER .         22      IN      A       192.0.2.1
If you use a static site generator to build your site locally and push the generated files to GitHub, pull the commit that added the CNAME file to your local repository. For more information, see "Troubleshooting custom domains and GitHub Pages."
Optionally, to enforce HTTPS encryption for your site, select Enforce HTTPS. It can take up to 24 hours before this option is available. For more information, see "Securing your GitHub Pages site with HTTPS." Enforce HTTPS for custom domains option
Configuring an apex domain
To set up an apex domain, such as example.com, you must configure a CNAME file in your GitHub Pages repository and an ALIAS, ANAME, or A record with your DNS provider.

If you are using an apex domain as your custom domain, we recommend also setting up a www subdomain. If you configure the correct records for each domain type through your DNS provider, GitHub Pages will automatically create redirects between the domains. For example, if you configure www.example.com as your custom domain for your site, and you have ALIAS and CNAME records set up for the apex and www domains, then example.com will redirect to www.example.com. For more information, see "Managing a custom domain for your GitHub Pages site."

On GitHub, navigate to your site's repository.
Under your repository name, click  Settings.
Repository settings button
Under "Custom domain", type your custom domain, then click Save. This will create a commit that adds a CNAME file in the root of your publishing source.
Save custom domain button
Navigate to your DNS provider and create either an ALIAS, ANAME, or A record. For more information about how to create the correct record, see your DNS provider's documentation.
To create an ALIAS or ANAME record, point your apex domain to the default domain for your site. For more information about the default domain for your site, see "About GitHub Pages."
To create an A record, point your apex domain to the IP addresses for GitHub Pages.
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
Open Terminal.
To confirm that your DNS record configured correctly, use the dig command, replacing EXAMPLE.COM with your apex domain. Confirm that the results match the IP addresses for GitHub Pages above.
$ dig EXAMPLE.COM +noall +answer
> EXAMPLE.COM     3600    IN A     185.199.108.153
> EXAMPLE.COM     3600    IN A     185.199.109.153
> EXAMPLE.COM     3600    IN A     185.199.110.153
> EXAMPLE.COM     3600    IN A     185.199.111.153
If you use a static site generator to build your site locally and push the generated files to GitHub, pull the commit that added the CNAME file to your local repository. For more information, see "Troubleshooting custom domains and GitHub Pages."
Optionally, to enforce HTTPS encryption for your site, select Enforce HTTPS. It can take up to 24 hours before this option is available. For more information, see "Securing your GitHub Pages site with HTTPS."
Enforce HTTPS for custom domains option
Further reading
"Troubleshooting custom domains and GitHub Pages"
Ask a human
Can't find what you're looking for?
Product
Features
Security
Enterprise
Case Studies
Pricing
Resources
Platform
Developer API
Partners
Atom
Electron
GitHub Desktop
Support
Help
Community Forum
Training
Status
Contact GitHub
Company
About
Blog
Careers
Press
Shop
© 2020 GitHub, Inc.
Terms
Privacy
