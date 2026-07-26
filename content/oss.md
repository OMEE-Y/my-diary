+++
title = "How I Started Contributing to Open Source"
date = 2026-07-26
+++

Before I start yapping, here's my GitHub:

[GitHub](https://github.com/OMEE-Y)

You can also check out my [merged PRs](https://github.com/search?q=is%3Apr%20is%3Amerged%20author%3AOMEE-Y&type=pullrequests)

# How I Started Contributing to Open Source

When I joined X, I started seeing developers contributing to open-source projects, getting PRs merged, and building things in public.

I had no idea how any of it worked.

So, like most beginners, I went to YouTube and searched:

> How to contribute to open source?

The process looked simple:

```text
Find an issue
→ Fork
→ Clone
→ Create a branch
→ Make changes
→ Test
→ Commit
→ Push
→ Open a PR
```

Simple enough.

But there's a difference between knowing how to open a PR and knowing what is actually worth contributing.

I learned that through experience.

# My First Merged PR

My first merged PR was in [Dodo Payments](https://github.com/dodopayments).

It was a small fix for `drizzle-kit` not loading `.env` and `.env.local` correctly. I updated `drizzle.config.ts` to load the environment variables using `dotenv`, with `.env.local` taking priority.

The PR was approved and merged.

That moment felt different.

It was the first time I had changed a real open-source codebase, had someone review my code, and seen that change become part of the project.

That's what got me hooked.

# From Using a Project to Improving It

After that PR, I spent more time exploring the Dodo Payments repositories.

While looking at the developer experience, I noticed that setting up Dodo Payments involved going through documentation and manually copying setup code depending on the tech stack.

I thought:

> Why not automate this?

So I built [`setup-dodo`](https://www.npmjs.com/package/setup-dodo), a zero-dependency CLI for setting up Dodo Payments integrations with Next.js, Express, and Better Auth.

I shared it on X:

<blockquote class="twitter-tweet">
<p lang="en" dir="ltr">
Tired of repeating the same <a href="https://x.com/dodopayments?ref_src=twsrc%5Etfw">@dodopayments</a> setup for every project.<br><br>
Built a zero-dependency CLI tool that instantly adds Dodo Payments to Next.js, Express, and Better-Auth apps.<br><br>
One command. Ready-to-use integration
<a href="https://t.co/QWHewKmqKW">pic.twitter.com/QWHewKmqKW</a>
</p>
&mdash; Om Yewale (@omee_y)
<a href="https://x.com/omee_y/status/2060669115279540696?ref_src=twsrc%5Etfw">May 30, 2026</a>
</blockquote>

<script async src="https://platform.x.com/widgets.js" charset="utf-8"></script>

Then Ayush Agarwal, founder of Dodo Payments, replied:

<blockquote class="twitter-tweet">
<p lang="en" dir="ltr">
This is great - we can add this command in dodo-cli too - do you mind opening a PR
</p>
&mdash; Ayush Agarwal (@ayushagarwal)
<a href="https://x.com/ayushagarwal/status/2060676402660454728?ref_src=twsrc%5Etfw">May 30, 2026</a>
</blockquote>

<script async src="https://platform.x.com/widgets.js" charset="utf-8"></script>

So I opened the PR.

[Dodo CLI PR #62](https://github.com/dodopayments/dodopayments-cli/pull/62)

It got merged and later appeared in the [v3.3.0 release](https://github.com/dodopayments/dodopayments-cli/releases/tag/v3.3.0).

I also got a shoutout from the maintainer:

<blockquote class="twitter-tweet">
<p lang="en" dir="ltr">
Thanks for the feature <a href="https://x.com/omee_y?ref_src=twsrc%5Etfw">@omee_y</a>!
</p>
&mdash; Sancho (@sanchogodinho)
<a href="https://x.com/sanchogodinho/status/2063908667729350711?ref_src=twsrc%5Etfw">June 8, 2026</a>
</blockquote>

<script async src="https://platform.x.com/widgets.js" charset="utf-8"></script>

That was a good lesson for me.

Sometimes the best contribution isn't sitting in the issue tracker.

You have to use the project, understand its users, and notice where the experience can be better.

# So, How Should You Start?

Here's what I'd recommend.

First, understand the project before touching the code.

Check the tech stack, repository structure, `README`, `CONTRIBUTING.md`, issues, existing PRs, tests, linters, formatters, and CI.

Don't treat GitHub issues like a treasure hunt.

`good first issue` is a great place to start, but once you understand the project, ask a better question:

> What can I improve here?

Maybe it's a bug.

Maybe it's documentation.

Maybe it's a missing feature.

Maybe it's repetitive setup that should be automated.

Think like a user, then think like a maintainer.

When you find something worth working on, keep the contribution focused.

```bash
git fork
git clone
git checkout -b fix/env-loading
```

Follow the project's contribution guidelines. Use the conventions already present in the repository. Run linting, formatting, tests, type checks, and builds before pushing.

Don't make the maintainer discover problems that you could have caught locally.

Then open a PR that clearly explains:

```text
What was wrong?
What changed?
Why was it changed?
How was it tested?
```

And when you get review comments, don't take them personally.

Your code working locally is only the beginning. The real challenge is making your change fit cleanly into a codebase you didn't build.

# What Open Source Taught Me

I started contributing because I wanted to get a PR merged.

I continued because I wanted to understand how real software is built.

Open source gives you something tutorials can't

You read code you didn't write

You work with maintainers

You learn project conventions

You see CI catch problems

You get your assumptions challenged in code review

You learn how small changes fit into a much larger system

That's the part I value most

The `Merged` label is nice

Understanding the codebase is better

