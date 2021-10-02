Dimboard
========

**This project only sort of works, and I've lost interest in it (read: resubsribed to
pinboard.in). As it stands I have no intentions of doing any more work on it (mainly
because I hate working with actions/ci shit). I wrote a fair bit of this README before
the project was ready for it... so if the following instructions below don't work, don't
be suprised**

GitHub-hosted [Pinboard](http://pinboard.in) alternative

**NOTE**: This project is still a fairly basic prototype, as such some values
are hardcoded, options aren't documented, etc.

## Why

I wanted to explore how I could make a free (as in beer, but also freedom) web
app with persistent (server-side) storage, and misusing GitHub's workflows
seemed like a fun and accessible way of doing it!

I don't genuinely reccomend using this project in your daily life... yet ;)

## Very-Quick-Start

**NOTE**: this method is not recommended for all users, before continuing
consider that:

 * This approach will affect your [profile's contribution stats](https://docs.github.com/en/github/setting-up-and-managing-your-github-profile/managing-contribution-graphs-on-your-profile/viewing-contributions-on-your-profile), as each new pin will create a new issue.

Unfortunately, there is currently no way to exclude certain repos from this
count other than to private them -- a feature which is disabled for forks. See
the Quick-Start section for instructions for making a private clone.

If this doesn't bother you:

* Fork the repository
* Enable [GitHub pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site) for the `main` branch.

## Quick-Start

As explained in the Very-Quick-Start section, you may want to create a private
copy of the repo.

To do so create a new private repository on GitHub called Dimboard (you can
call it anything, just make sure to adapt the `push` command below), and run
the following (adapted from [GitHub Docs - Duplicating a repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/duplicating-a-repository#mirroring-a-repository))

```sh
git clone --bare https://github.com/dylan-lom/Dimboard
cd Dimboard
git push --mirror https://github.com/$YOUR_GITHUB_USER/Dimboard
cd ..
rm -rf Dimboard
```

Now enable GitHub pages on your Dimboard private repo (see Very-Quick-Start).

**NOTE**: This assumes that your [private contributions are hidden](https://docs.github.com/en/github/setting-up-and-managing-your-github-profile/managing-contribution-graphs-on-your-profile/publicizing-or-hiding-your-private-contributions-on-your-profile). This is the default behaviour at the time of writing.

