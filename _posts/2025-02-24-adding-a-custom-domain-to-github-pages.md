---
title: Adding a custom domain to GitHub Pages
date: 2025-02-24 10:00 PM -05:00
categories: [GitHub Pages]
tags: [github pages]
---

In this post, I'm going to go over the steps I took to add a custom domain to my GitHub Pages site.

## Step 1: Register domain

The first thing I did was register my domain, `aaronjadkins.com`, with <a href="https://porkbun.com/" target="_blank">Porkbun</a>.

## Step 2: Add domain to GitHub Pages

I added my domain to GitHub Pages by going to my GitHub Pages repository > settings > pages (under code and automation), typing `aaronjadkins.com` into the custom domain field, and clicking save. It then showed that a DNS check was in progress.

![GitHub Pages custom domain field](https://res.cloudinary.com/do8uy1fxa/image/upload/v1740333794/adding-custom-domain-on-github-pages_erhbw2.png)

## Step 3: Configure DNS records

The next step was to configure the domain's DNS records. This process was fairly simple thanks to Porkbun's quick DNS configuration. However, if your domain registrar doesn't have a quick DNS configuration, you can refer to the GitHub Pages <a href="https://docs.github.com/en/pages" target="_blank">documentation</a> for help with managing DNS records.

To configure the records, I navigated to the domain management settings on Porkbun and clicked on DNS records. Then I scrolled down to the quick DNS configuration section and clicked on GitHub.

![Porkbun's quick DNS configuration section](https://res.cloudinary.com/do8uy1fxa/image/upload/v1740333844/porkbun-quick-dns-configuration_tejfjc.png)

This added the standard `A` and `AAAA` records, and for the `CNAME` record, I set the host value to `www.aaronjadkins.com` and the answer field value to `adkinsa.github.io`. After I was finished, this is what the DNS records looked like:

![DNS records for aaronjadkins.com](https://res.cloudinary.com/do8uy1fxa/image/upload/v1740333816/domain-dns-records_h5muzw.png)

## Step 4: Update URL in _config.yml

Next, I went to the `_config.yml` file in my sites root directory and updated the URL to `https://aaronjadkins.com`.

## Step 5: Enforce HTTPS

Finally, once the DNS check was successful, I selected the option to enforce HTTPS.

![GitHub Pages settings page showing DNS check successful and Enforce HTTPS checked](https://res.cloudinary.com/do8uy1fxa/image/upload/v1740454722/github-pages-settings-dns-check-successful-and-enforce-https-checked_placyj.png)

The site is now live at <a href="https://aaronjadkins.com/" target="_blank">https://aaronjadkins.com/</a>.