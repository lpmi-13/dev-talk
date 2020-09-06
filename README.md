# Dev Talk

The point of this project is to create a very basic corpus (possibly corpora) of dev-talk
in various podcasts so we can see what shakes out.

## data sources (podcasts)

We need both transcripts and audio (for the force alignment to create audio materials later), so trying to target the following podcasts:

- Arrested Devops
(https://www.arresteddevops.com/)

some of the episodes have transcripts...investigating how easily otter.ai can create audio transcripts

answer: the generated transcripts are usable, but we only get 600 minutes free per month, and each episode is about 60 minutes, so that's only 10 episodes...will probably grab the low-hanging fruit first

- Software Engineering Daily
(https://softwareengineeringdaily.com/2017/04/21/21-with-balaji-srinivasan/)

transcripts seem available from 2017-ish (possibly earlier), and REST API, so easy to traverse

- Shop Talk Show
(https://shoptalkshow.com/325-code-expensive/)

transcripts available from 325 onwards

- Darknet Diaries
(https://darknetdiaries.com/episode/1/)

all episodes have full transcripts

- JamStack Radio
(https://www.heavybit.com/library/podcasts/jamstack-radio/ep-1-introducing-jamstack-radio/)

all episodes have full transcripts

- Talk Python to Me
(https://talkpython.fm/episodes/show/1/eve-restful-apis-for-humans)

all episodes have full transcripts

- Screaming in the cloud
(https://www.lastweekinaws.com/podcast/aws-morning-brief/networking-in-the-cloud-fundamentals-part-4/)

the newer episodes have transcripts, haven't figured out where those started yet...


- Code Newbie
(https://www.codenewbie.org/podcast/intro-to-accessibility)

all episodes from S1E1 (which is halfway up the page for some reason), have transcripts

- Command Line Heroes
(https://www.redhat.com/en/command-line-heroes/season-1/os-wars-part-1)

all episodes have transcripts

- Ladybug Podcast

episodes are at https://www.ladybug.dev/episodes/

transcripts at https://github.com/ladybug-podcast/ladybug-website/tree/master/transcripts

- Base CS Podcast
(https://www.codenewbie.org/basecs/19)

transcripts available fro season 3

...this one might be better to cross-reference with the terms that fall out of the vector comparison for specialty terms


## data collection

mostly scraping. Once the majority of what we want is compiled, will see about adding a github action to watch for changes in the RSS feed maybe? Then grab new content? Honestly, there's easily enough already up to get something useful worked up already.

We'll probably also need to group the above resources by rough topic area just so the distributions are possible to describe easily (eg, the Talk Python to Me podcast will generate data that's skewed towards python, obviously, and the resulting materials might be of less interest to java programmers)

## purpose

While a corpus compiled of how developers write (like README's, source code comments, or documentation) is useful and necessary, it is highly likely that the way developers actually talk is different in numerous ways

- vocabulary/grammatical structure/function for communication/discourse structure (along with other purely conversational elements like turn-taking behavior)

In order to create materials to teach new developers how to "talk like a developer" (something that's moreso of interest to non-native speakers), it's necessary to first figure out how developers actually talk.

Unfortunately, there's no easy way to get spoken corpora constructed for how devs talk in the workplace, so the next best thing is to compile this data from
freely available sources from roughly similar registers.

Once we've got the data, it should be possible to create material to practice listening (if not speaking...mostly since giving feedback in an automated manner is easier for listening materials...we can assess knowledge/comprehension outcomes fairly easily) as well as reading materials, probably focused mostly on vocabulary.

It's not entirely outside of the realm of possibility that this data might eventually inform some sort of formal "How to talk like a developer" course, but that's a long way off for the present.
