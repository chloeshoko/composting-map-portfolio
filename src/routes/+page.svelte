<!--
@component
This is your page!
-->
<script>
  // Import all the news furniture components
  import ArticleHeader from '$lib/components/ArticleHeader.svelte';
  import ArticleBody from '$lib/components/ArticleBody.svelte';
  import DropoffMap from '$lib/components/DropoffMap.svelte';
  import Image from '$lib/components/Image.svelte';
  import ReadMore from '$lib/components/ReadMore.svelte';
  import Timeline from '$lib/components/Timeline.svelte';
  import ContextBox from '$lib/components/ContextBox.svelte'; 

  let { data } = $props();

  // Article metadata
  let headline = 'Mayor-Elect Mamdani Signals the City Will Keep Mandatory Composting';
  let byline = 'Chloe Shoko Rogers';
  let pubDate = '2025-12-18';
</script>

<!-- This sets the page title in the browser tab -->
<svelte:head>
  <title>{headline} | NYCity News Service</title>
  <meta name="description" content="At the Craig Newmark Graduate School of Journalism at the City University of New York, change is in our DNA. That comes of being born in 2006, as the digital revolution was transforming our profession in ways none of us could have imagined." />
</svelte:head>

<!-- Your page content goes here -->
<div class="container">
  
  <!-- Article Header: Headline, byline, and publication date -->
  <ArticleHeader
    {headline}
    {byline}
    {pubDate}
  />

  <!-- Lead Image: Animated gif of students at the journalism school -->
  <Image
    src="/bins.JPG"
    alt="The Craig Newmark Graduate School of Journalism is at 219 West 40th Street in Midtown Manhattan."
    caption="New York City waste bins"
    credit="Chloe Shoko Rogers"
  />

  <!-- Article Body: The main story text with proper typography -->
  <ArticleBody>
    <p>
      Mayor-elect Zohran Mamdani has signaled that New York City will maintain its requirement that residents separate their organic waste — food scraps, compostable paper and yard trimmings — from other trash. 
    </p>

    <p>
      The organic waste is processed into compost or renewable energy, a key component of reducing the city’s carbon footprint and the amount of waste sent to landfills. The Department of Sanitation states that residents can be fined up to $300 for noncompliance. But Mayor Eric Adams paused most enforcement just weeks after ticketing began in April, saying fines would resume sometime in 2026. 
    </p>
     
    <p>
      Under Adams’ pause, enforcement is paused for most buildings, except for those with more than 30 units that receive four warnings. The agency continues to issue warnings to residents in buildings of all sizes as an educational reminder that participation is mandatory, but fines are not being issued at this time beyond that exception.
    </p>

    <Timeline
      events={[
        {
          date: 'October 2024',
          description: 'New York City required residents to separate organic waste from their trash'
        },
        {
          date: 'April 1, 2025',
          description: 'Ticketing for noncompliance began'
        },
        {
          date: 'April 18, 2025',
          description: "Mayor Eric Adams paused fines, saying they\'d start back up sometime in 2026"
        }
      ]}
    />

    <p>
      With fines set to resume sometime in 2026 and a new mayor taking office in January, the future of enforcement is uncertain. Meanwhile, the city is capturing only 10 percent of its organic waste — a fraction of what it needs to meet its goal of sending zero waste to landfills by 2030."
    </p>
    <p>
      Asked how he would handle the issue, Mamdani said at a press conference on December 9th, “we have to fully follow through on the policies we have,” adding that there is “a fatigue with constantly changing policies in New York City and an inability to follow through.” 
    </p>

    <p>
     New Yorkers have been required to separate organic waste since October 2024. When ticketing for noncompliance began in April 2025, the residential organic waste capture rate increased by nearly 200 percent, rising to more than 9,000 tons in April from about 3,100 tons in March, according to NYC Open Data. 
     </p>

     <iframe title="Residential Food Waste Collected in NYC, 2025 (tons)" 
     aria-label="Line chart" 
     id="datawrapper-chart-XNbGX" 
     src="https://datawrapper.dwcdn.net/XNbGX/4/" 
     scrolling="no" 
     frameborder="0" 
     style="width: 0; min-width: 100% !important; border: none;" 
     height="410" data-external="1"></iframe>
     <script type="text/javascript">window.addEventListener("message",function(a){if(void 0!==a.data["datawrapper-height"]){var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r,i=0;r=e[i];i++)if(r.contentWindow===a.source){var d=a.data["datawrapper-height"][t]+"px";r.style.height=d}}});
    </script>

    <p class="chart-transition-paragraph">
     Enforcement halted in April and while the capture rate gradually decreased between May and October, November’s totals reached record highs, according to the Department of Sanitation. Even so, the city is only capturing a fraction of its organic waste. 
     </p>

     <div class="datawrapper-map-box">
      <iframe title="Organic Waste Collection Spiked Across NYC When Fines Began in April 2025" 
      aria-label="Choropleth map" 
      id="datawrapper-chart-ElVSn" 
      class="datawrapper-map-frame"
      src="https://datawrapper.dwcdn.net/ElVSn/3/" 
      scrolling="no" 
      frameborder="0" 
      style="width: 0; min-width: 100% !important; border: none;" 
      height="800" 
      data-external="1">
      </iframe>
    </div>
     <script type="text/javascript">window.addEventListener("message",function(a){if(void 0!==a.data["datawrapper-height"]){var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r,i=0;r=e[i];i++)if(r.contentWindow===a.source){var d=a.data["datawrapper-height"][t]+"px";r.style.height=d}}});
    </script>

    <p>
      Michael Crorkin, 25, the superintendent of an 18-unit apartment building in Murray Hill, said fines are “absolutely necessary,” arguing that without them, a lot of buildings would avoid complying.
    </p>

    <p>
     Still, he says most residents either don’t want to separate organics or don’t know how to do it properly. 
     </p>

    <p>
      “Just based on what I’ve seen with regular garbage and how they can’t even separate recycling like plastics and paper from regular waste, I don’t think they’re gonna take the time to compost,” Crorkin said. He added participation might increase if tenants were provided small in-unit compost bins, making separation easier to build into their daily routines. 
    </p>

    <p>
      Crorkin's skepticism is borne out by the numbers — the city is only capturing about 10 percent of its organic waste. Samantha MacBride, a professor at Baruch College who teaches sustainability, said that means a significant portion of the city's roughly $500 million annual waste export budget is spent transporting organics to landfills that could have been diverted.
    </p>

    <p>
      MacBride said the core issue is a lack of effective education by the Department of Sanitation. While the department said in a request for comment that it has conducted a “massive amount of public education including knocking on nearly 800,000 doors,” MacBride said that the department has failed to work with owners and managers of apartment buildings to increase participation, noting that they are only required to place the correct bins outside.
    </p>

    <p>
      “ There’s a far cry between doing that and actually getting a system going in your building where some or most of the people are contributing their food scraps,” she said. 
    </p>

    <p>Marisa DeDominicis, co-founder and executive director of the community composting organization Earth Matter, said that the city should prioritize education starting as early as kindergarten. She said it’s more effective for people to understand why composting matters and how they can participate so they “feel good about their actions” rather than having stress or anxiety about getting a fine. 
    </p>

    <p>
      Meanwhile, the City Council’s Common Sense Caucus is pushing to eliminate the mandate to separate organic waste altogether, arguing that participation should be voluntary.
    </p>

    <p>
      “Forcible mandates are wrong every time, whether they are forced vaccinations or mandated composting,” said Joann Ariola, caucus co-chair and council member. “People should still be free to choose. This is still America.”
    </p>

    <ContextBox
      title="In addition to curbside pickup, how else can New Yorkers drop off their food scraps?"
      items={[
        "The city has 400 bright orange Smart Composting Bins, accessible 24/7 via the free NYC Compost app. They accept all food scraps and plant waste, including meat, dairy, and prepared foods.",
        "More than 200 additional drop-off sites at community gardens, parks, schools, and nonprofits are also available across the five boroughs — but most do not accept meat, dairy, or prepared food. Hours and accepted materials vary by site.",
      ]}      
    />

    <DropoffMap points={data.dropoffs} />

    <ReadMore title="About the map data">
      <p>
        This map uses <a href=https://data.cityofnewyork.us/Environment/Food-Scrap-Drop-Off-Locations-in-NYC/if26-z6xq/about_dataNYC>NYC Open Data</a> on Food Scrap Drop-Off Sites from the Department of Sanitation.
        It currently includes {data.dropoffs.length} locations with valid coordinates.
      </p>
    </ReadMore>
  
</ArticleBody>

  

</div>

<style>
  .container :global(article.article-body p.chart-transition-paragraph) {
    margin-top: var(--spacing-lg);
    margin-bottom: var(--spacing-xl);
  }

  .datawrapper-map-box {
    margin: var(--spacing-sm) 0 var(--spacing-md);
    padding: var(--spacing-sm);
    background: var(--color-white);
    border-radius: var(--border-radius-sm);
  }

  .datawrapper-map-frame {
    display: block;
  }
</style>
