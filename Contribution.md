## Contribution
Github has been one of my favorite tools as a developer. Checking some of its pages, I realized that under the explore tab, you can discover different repositories, events or developers that maybe you did not have under the scope. All pages look great, they are fresh, easy to read and well distributed. However, there's one page that looks different than the rest.

This page is the [explore](https://github.com/explore) page. It does not have a hero area, like the others, and the info looks a bit messier if you compare it with the others. It does have a main section in the middle, where you can see all the data feed related to your profile, but there are some asides that make it harder to read it. As well there is a lot of use of borders in general, which tries to get all time the attention for every new input that it comes, making the reader tired to continue after a couple of scrolls.

## Check Other data feed
Comparing with other data feed. I took a deeper look at: 

 - Facebook
 - Twitter
 - Gitlab

I analyzed what do they have in common at the moment you check a data feed to understand what's new in your timeline. For social media (Facebook, and Twitter) are always sorting their info with a rounded pic of the avatar, making it less aggressive, and becoming a global standard in our daily browsing. They are also showing some basic info about the user, followed by some space to show then the content. 

Regarding GitLab, they explore to get all the info gathered by tiny rows, showing a bit edgier avatar pic. One important detail to notice here is the way they tried to make everything homogeny, which unfortunately plays against the goodwill, making it quite difficult to understand, when you are checking for a concrete repository or user.

My conclusion: The way to modernize the explore page, is applying the new style guide that Github owns, and apply some small additions inspired by the pages mentioned above.
## The idea
Please, check my proposal for the new explore page.

### [Check it out](https://ruffeng.github.io/Github-explore/)

My idea was mainly to adapt the explore page to be closer to the other pages. That means adding a hero area, assuring in which page are you right now, and a small headline.

Notice that now, the sidebars are the main focus, distributed into 3 cards. All this information is quite important for the user and could be ignored in the current design of the page. I wanted to boost it, giving importance to the content and going with a minimal UI to not distract the users from the information. As well it's important to say that this page is encouraging to go for less edgy images, and borders, with new rounded images, making the look and feel more friendly.

After the 3 cards, the data feed comes into your timeline. It tries to get out of the borders, and introduce light colors to make it more accessible and easy to read. 

The trending developers now come with a follow button, which makes it easier to directly follow them and have updates.

## The design

I tried to apply all the [primer design system](https://primer.style/) styles. I really appreciate you are opening this design system, it really helped me a lot.

## Responsiveness

This page implements a small solution for responsiveness, which does not escalate well when the code grows up. I decided to go with this solution, purposed some time ago by [Mikolaj Dobrucky](https://css-tricks.com/responsive-designs-and-css-custom-properties-building-a-flexible-grid-system/). The main option was to set some CSS-grid property and apply some media queries, but my idea was to make only the 3 top with a different display based on the viewport. So no need for a bunch of media queries. The rest of the cards are auto-responsive, so they should adapt. The sticky menu is removed from mobile into tablet, because in the current page there's no solution for that, and I wanted just to insert this navigation in order to display it more close to the real page. But was not my intention to rebuild that component

I would say for this project, this solution fits well. In order to grow up. It would be interesting to spend more resources (time/effort) to build a solid and robust solution.

## The code
Please, [check out the code](https://github.com/Ruffeng/Github-explore). The stack I decided to do is:

 - Middleman (static generator in Ruby)
 - SCSS

It's been around 1 year without developing in Ruby, and around 2 without developing with the ERB template engine. So please, take into consideration I was a bit rusty here. Middleman does not provide controllers or models, which I had to create a couple of variables in some views.

Usually, my main stack is React. But then, why did I decide to go for Ruby + Middleman? -Well, I wanted to prove myself that I still remember Ruby, and wanted to prove as well that I am able to build scalable applications even if they are not my main ecosystem currently.

I was thinking to do it in React, using the full design system that [primer is providing to me](https://primer.style/components/). I feel much stronger there, making a better component composition than ruby ( and its yield). But I love challenges, and I think was worth it to do it in Ruby, since Github has its own stack in it. My idea with React would be the design system and some styled-components for some paddings. 

What about JS? This page does not contain any JS currently. Since it's a proposal to display how I would imagine this page, I went more into the direction to show a UI.  There are some good improvements here like all the clicks are doing async all the actions we are waiting for. But I wanted to focus on display a final page, and be able to contribute with some ideas.

What about tests? In this project, there are no tests. Usually, in my environment, I test with [testing-library](https://github.com/testing-library) ( I love this library), under  Jest environment and as well some browser tests with [webdriverio](https://github.com/webdriverio/webdriverio). However, since here there's a few call to actions (which mainly are just clicks to go to the repository or use page), I didn't go for it. If I would have time, I would focus on make it in Rspec in case of Ruby (I hope I still remember something regarding Rspec). Please, consider me as a person who loves to test its apps, but because of time pressure to show this page, I decided to be pragmatic and finish the page as soon as possible.

## Improvements

Definitely, I would love to spend more time making this page nicer, and better. There are some small 'gotchas' that needs to be improved:

 - Tests. Since it's a single page, I would go for unit and integration tests. No more further.
 - All CTA doing something (currently some of them are just for display purposes)
 - More testing with different browsers. I tried Edge/Chrome/Safari/Firefox for Desktop and Android/iPhone for mobile. I've found some small details (especially for Safari) that could be improved. I would love as well test properly in  IE11 but didn't have enough time for it. Usually, I like to take care that it works in most of the browsers, and definitely [caniuse](https://caniuse.com/) it's one of my best friends to check that what I am writing is supported
 - Some UI changes. I would love to test more UI changes and see different combinations to explore new ways. As I said, I focused on the page and the idea I had in mind.

## Motivation 
As you can see, my commitment and motivation are really high. Please consider me to be part of your team, and I can assure you, you won't be disappointed!
