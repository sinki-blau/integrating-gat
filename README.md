Open source tools for geographic analysis in transport planning
================
2020-08-04

<!-- should be integrated in transport planning tools. -->

<!-- --- software for transport data analysis, modelling and visualisation --- -->

<!-- workflows in academic, public sector and private consultancy transport planning contexts still tend to separate vital geographic processing and map making stages from the rest of the analysis. -->

# Abstract

<!-- Tools for geographic analysis have long been used in transport planning. -->

<!-- , alongside other (typically primarily economic and engineering) considerations. -->

<!-- Transport is inherently geographic, involving the movement of people and goods between places along spatial networks. -->

Geographic methods have long supported transport planners to develop
effective and evidence-based interventions that are appropriate to local
contexts.
<!-- Decarbonising transport systems is vital for the future. -->
<!-- Yet geographic analysis is often treated as an optional 'add-on'  transport data analysis and modelling. -->
<!-- This dichotomy, between 'geographic' and 'non-geographic' analysis in transport planning is undesirable because it: -->
<!-- (1) reduces researcher effectiveness due to the time-consuming process of 'context switching'; -->
<!-- (2) prevents reproducibility, requiring installation and management of geographic and non-geographic tools; and  -->
<!-- (3) hides vital geographic components in transport plans, with adverse consequences for interventions that can benefit from being placed where they are most needed. -->
Many popular ‘tools of the trade’ for geographic analysis used in
practice are proprietary, reducing access to the benefits of methods
such as spatial interaction <!-- transport demand --> modelling, routing
and route network analysis. <!-- to estimate the impacts of change, -->
<!-- --- from policies encouraging car sharing to investment in geographically specific sustainable transport infrastructure networks --- -->
<!-- in terms of the economic, social and environmental benefits of different scenarios. -->
<!-- The continued dominance of closed software in the field -->
<!-- --- at a time of innovation in computer hardware and software and uptake of open source software in fields such as data science --- -->
<!-- also has negative consequences in terms of reproducibility, transparency, scalability of solutions and public participation in the wider transport planning process. -->
<!-- or difficult to integrate into the wider planning process or both. -->
In this context, the aim of this paper is to explore emerging open
source
<!-- , with a focus on geographic data analysis, routing and route network analysis. -->
tools for geographic analysis in transport planning, with reference to
the literature. A key finding is that a growing number of open source
options exist. These can be classified as command-line interface (CLI),
graphical user interface (GUI) or web-based tools, instances of which
can be accessed remotely or set-up locally. Open source tools for
transport planning come in many forms, ranging from single functions
dedicated to a particular task to large software projects and enabling
geographic analysis at every stage of the transport planning process,
from data collection and demand modelling to visualisation of results on
publicly available and interactive web-based maps. Although options are
abundant, many lack documentation explaining how they can be used ‘in
production’ and few case studies exist showing how they can support
established transport planning workflows. Thus, while open source tools
for geographic analysis in transport planning *as they exist today* hold
great promise, their *future potential* is even greater. There are many
ways for developers, researchers, practitioners and the interested
public to participate and ‘fill gaps’ in the emerging landscape,
particularly in relation to: integration and cross-compatibility of
diverse tools; accessible tutorials; and real world case studies
published in the academic literature. The paper concludes that time
invested in developing open source tools and associated ‘communities of
practice’ is time well-spent.
<!-- such as MATsim and SUMO (which have limited geographic analysis capabilities), in addition to more general programs such as QGIS, as well as open source languages such as R and Python which are used as the foundation of a growing number of 'packages' for transport planning. -->
<!-- Due to the size and rapidly evolving state of the software landscape for transport planning, the paper cannot be complete in its coverage. -->
<!-- However, the focus on a specific aspect of transport planning --- geographic analysis --- highlights themes, such as ease-of-use and community support, that may be relevant to other branches of the planning process. -->
<!-- In light of the rapid growth in the size, number and quality of open source tools for transport planning, there has never been a better time for transport planners to adopt open source solutions end-to-end in their everyday practice. -->
<!-- notwithstanding institutional barriers,  -->
<!-- Each ecosystem is found to provide numerous 'tools of the trade' for integrating geographic analysis in transport research, some of which are already being used in practice. -->
<!-- In addition to integrating geographic considerations, the shift to such open source solutions will have wider benefits for reproducibility, transparency and democratic accountability in transport planning. -->
<!--  transport planning experts and the public alike, -->
<!-- Ultimately, by highlighting cost effective and geographically targeted interventions, integrating geographic analysis in transport planning could lead to better decision making. -->
<!-- and support the global efforts to transition away from fossil fuels and towards a healthy, low carbon transport system. -->

<!-- ### Notes/questions -->

<!-- This paper is work in progress and its focus has shifted over time. -->

<!-- A previous working title was "Integrating geographic analysis in transport planning: new open source tools for the trade". -->

<!-- The need to integrate geographic analysis in transport planning is still a central theme of the paper but the focus is now on solutions, in the form of open source software. -->

<!-- Does the paper now have too much on the importance on integrating geographic analysis in transport planning, given the new emphasis? -->

<!-- And are there any other open source software projects I should include, within or in addition to the overview of the three ecosystems selected? -->

# Introduction: geographic analysis in transport planning

<!-- : the importance of geographic analysis in transport planning -->

<!-- Should that heading omit the "Introduction:" part? -->

Transport planning is an applied discipline involving developing local
policies and the design and placement of physical infrastructure
including ways — highways, railways, cycleways and footways — for the
greatest economic, social and environmental benefit (O’Flaherty and Bell
1997; Parkin 2018). Planning also involves thinking about the future,
envisioning scenarios of change and making the
<!-- economic and political --> case for change (Timms, Tight, and
Watling 2014). Successful transport plans are therefore a combination of
geographically specific recommendations (e.g. “build this way here”) and
long-term strategies guided by citywide, regional and national visions
(e.g. “imagine the benefits of making the city free from private cars by
2030”). The rewards can be great: transport planners who have designed —
and helped to implement — plans appropriate to the needs of an area
leave a legacy that will benefit people and the environment for
generations to come.\[1\]

Transport planning can be considered as “more of an art than a
technique”, although *good* transport plans also rely on robust
analysis and modelling of sometimes large and usually spatial input
datasets (Dios Ort’uzar S. and Willumsen 2011). Ways and other pieces of
transport infrastructure must *go somewhere*; transport planning
involves consideration of where investment and other interventions are
most needed. Tools for geographic analysis have been used in transport
planning since at least the 1990s, when local transport planning bodies
in the United States started using geographic information systems (GIS)
software to support their transport planning activities (Anderson 1991),
taking advantage of newly available software and hardware such as the
Intel 80386 processor (first released in 1985) which could run early
proprietary GISs such as ‘SPANS’ (Ebdon 1992).

Despite the inherently geographic nature of movement, and the growth of
GIS in transport planning, the importance of geographic in transport
systems has long been overlooked (Rodrigue, Comtois, and Slack 2013),
notwithstanding efforts to formalise the field of ‘GIS-T’, described in
the next section. Geographic methods — such as origin-destination
modelling, route assessment and spatial network analysis — are prominent
in the literature, providing evidence for a range of transport planning
interventions (e.g. Jäppinen, Toivonen, and Salonen 2013; Larsen,
Patterson, and El-Geneidy 2013; Tribby and a. Zandbergen 2012). But
there has been less research into digital geographic *tools*, as
discussed in Section <a href="#the-current-landscape">3</a>, despite the
fact that geographic methods must be accompanied by software and a user
interface if they are to be of use in practice.

A range of data driven transport planning approaches has evolved in
recent years to take advantage of new datasets and technologies. Large
movement datasets from disruptive ‘ride hailing’ firms have been used to
better understand parking patterns (Aryandoust, van Vliet, and Patt
2019); ‘deep learning’ has been used to forecast demand for transport
services in near real-time (Liao et al. 2018). Such novel geographic
approaches can be defined as Geographic Data Science, a still emerging
field that calls for the tighter integration between data science and
geographic research (Singleton and Arribas-Bel 2019). While there is
much academic activity in this direction, the extent to which new
geographic tools have gained traction in practice, and in transport
planning practice in particular, is debatable. In this context, the goal
of this paper is to add to the literature on geographic tools in
transport planning, with a focus on open source options.

At this point some definitions are in order. Although ubiquitous in the
literature, terms such as ‘tool’, ‘software’ and ‘model’ are often used
interchangeably, relying on the (potentially unsafe) implicit assumption
that everyone shares the same idea of what they mean (see Salter et al.
2009 for an example). For the purposes of this paper, a **tool** is a
broad term referring to a modular piece of software or online service; a
**model**, by contrast, is method or process that is expounded in
theoretical terms; **software** is the collection of computer
instructions that underlies digital tools, encoded in publicly available
and transparent programming languages (in **open source software**) or
in a ‘binary’ file that has “limits against usage, distribution, and
modification that are imposed by its publisher” (Dhir and Dhir 2017),
the inner workings of which are obfuscated from the user (in
**proprietary software**). An increasingly used but seldom defined term
in this context is **ecosystem** which, following Franco-Bedoya et al.
(2017), we define as the wider community of people organizations that
support the development of open source software. The paper focuses on
tools, as opposed to software or software ecosystems, because tools are
tangible and widely understood (unlike software ecosystems) entities
that the end user sees (as opposed to software, which is a rather
esoteric concept).

<!-- Transport planning is embedded within broader democratic processes *and* local geographic contexts. -->

The focus on *open source* tools for geographic analysis in transport
planning is timely because this is an area of rapid growth, as outlined
in Section <a href="#open-source-tools">4</a>. The topic has yet to be
explored in the academic literature, to the best of the author’s
knowledge. A deeper reason that transport planning benefits from levels
of transparency and citizen participation that are more easily reached
with open source solutions than proprietary solutions (Peters 2020).
Transport planning involves decisions about how public funds, spaces and
other shared resources are used. It is, to a greater or lesser extent,
part of wider democratic processes that reflect contemporary political
and societal priorities (Legacy 2016). These priorities have shifted
substantially over the past few decades, meaning that transport plans
based on out-of-date ideas or faulty model assumptions (such as the
assumption that congestion can be tackled by building more roads) can
lead to unwanted impacts (such as increased congestion), which can be
fatal (Hollander 2016).

The importance of transparency and democratic accountability in
transport planning (and hence the importance of open source tools in
transport planning) has increased alongside wider campaigns for
evidence-based decision making and ‘participatory democracy’ (Monbiot
2017; Hackl et al. 2019), and growing evidence that transport systems
cause substantial damage to the environment and human health and
wellbeing. Roads are now the “leading cause of death for children and
young adults aged 5-29 years” with 1.35 million people killed and tens
of millions injured and disabled each year due a range of factors
including unsafe speeds, weak road traffic laws, lack of enforcement and
poor infrastructure that forces pedestrians and cyclists to mix with
motorised modes (World Health Organization 2018). The air pollution
impacts could be even greater, with a growing body of research linking
air pollution to Alzheimer’s disease, lung cancer and heart disease
among hundreds of millions of sufferers worldwide (Kampa and Castanas
2008; Kilian and Kitazawa 2018). Transport is responsible for a quarter
of global greenhouse gas emissions and growing (Harrison and Hester
2017), and is one of the hardest sectors to decarbonise (Moriarty and
Honnery 2008), meaning that reducing transport energy use is an urgent
priority.
<!-- affecting the global population, especially the projected 1.4 billion people who will live in low elevation (less than 10 m above sea level) coastal zones by 2060 [@neumann_future_2015]. -->
<!-- Transport planning has the potential to improve health outcomes. -->
<!-- Motor traffic can be reduced and redirected to minimize the amount of pollution that reaches vulnerable lungs. -->
<!-- Transport planning can have positive health impacts by enabling millions of people to integrate physical activity into their everyday lives, thereby tackling the 'obesity crisis' [@yang_travelobesity_2013]. -->
<!-- Another entrenched global challenge in the 21^st^ Century is social and economic inequality. -->
<!-- Transport planning can tackle inequality by prioritising modes that are accessible to a wide range of people, from '8 to 80 year-olds'.^[The term "from 8 to 80 year olds" is used informally by transport planning practitioners to convey their intention to design for everyone, as exemplified by the use of the phrase in a 2015 article in the [Guardian](https://www.theguardian.com/uk-news/davehillblog/2015/sep/23/whitechapel-high-street-cycle-superhighway-bus-stop-bypass-is-a-mess).] A recent policy driver of transport planning is climate change mitigation. -->

Transport planning is inherently embedded within local geographic
contexts because transport systems, and associated networks of physical
infrastructure, are highly localised (Barth’elemy 2011; Levinson 2012)
and to some degree dynamic (Xie and Levinson 2011) phenomena. Transport
planning is therefore fundamentally a *geographic activity*. All
accurate geographic coordinates are defined with reference to the
Earth’s surface, either via geographic or projected coordinate systems
(Sherman 2008). By extension, transport planning is a geographic
enterprise.

The influential textbook *Modelling Transport* outlines the main stages
of transport planning as follows (Dios Ort’uzar S. and Willumsen 2011).

1)  problem formulation
2)  data collection
3)  modelling/analysis
4)  evaluation
5)  implementation of solutions

Each of these stages, illustrated in Figure
<a href="#fig:schematic">1</a>, has geographic components. The
3<sup>rd</sup> stage, can refer to at least three distinct processes:
the ‘four stage’ transport model (left box); statistical modelling
(central box) or geographic analysis and modelling (right box, Figure
<a href="#fig:schematic">1</a>). The wider point is that geographic
techniques can supplement and in some cases replace traditional
modelling, and the classic four stage transport model. Many of the
inputs (datasets with geographic coordinates) and outputs (maps and
geographically specific recommendations) shown in Figure
<a href="#fig:schematic">1</a> are spatial, suggesting the importance of
geographic tools throughout the transport planning process.

<div class="figure">

<img src="flow-diagram.png" alt="Schematic diagram illustrating the modelling process, geographic analysis and the four-stage in the context of the wider transport planning process (adapted from Ortúzar and Willumsen, 2011, with the 'Geographic analysis and modelling component' added for this paper)." width="100%" />

<p class="caption">

Figure 1: Schematic diagram illustrating the modelling process,
geographic analysis and the four-stage in the context of the wider
transport planning process (adapted from Ortúzar and Willumsen, 2011,
with the ‘Geographic analysis and modelling component’ added for this
paper).

</p>

</div>

**Formulation of the problem** (stage 1 in the transport planning
process illustrated in Figure <a href="#fig:schematic">1</a>) and
identification of the scope of solutions that the transport planning
process can propose is inherently geographic. The first step of many
projects is defining the ‘region of interest’. This step has important
implications because it can focus the analysis on areas where solutions
are most likely to be implemented and, conversely, highlight the
potential for inter-regional collaboration. Although the region of
interest may be pre-determined by administrative boundaries over which a
planning authority presides, geographic analysis this first stage in the
transport planning process can help refine the definition of the ‘region
of interest’ to include different ‘spheres of influence’ such as the
wider catchment area, the administrative region, and the area that is
the focus of the study.
<!-- Defining, demarcating and visualising the study region in a more nuanced way could... -->
<!-- Todo: could add (e.g. the city centre) and other comments to each sphere comment. -->
<!-- To take one example, in a project where the study region was Leeds city centre... -->

**Data collection** (stage 2) is an explicitly geographical activity,
although in some cases the geographic components of valuable data are
not used (origin-destination datasets in which the coordinates of
origins and destinations are excluded represent a common example).
Geographic analysis tools can support this stage not only by providing
descriptive overviews of the datasets available to planners (and their
limitations such as parts of a city lacking in data), but by flagging
places where additional monitoring is needed (e.g Lindsey et al. 2013).

Likewise, **modelling** (stage 3) is a central component of data-driven
transport planning. Whether the modelling involves a four stage model,
statistical modelling or geographic analysis, it inevitably contains
some geographic analysis.
<!-- (in the 21^st^ Century this stage could more usefully be called **modelling and data analysis**). -->
Geographic analysis is implicit in the classic four-stage model: 1) trip
generation (the number of trips generated by each zone in a region) is
influenced by geographic factors such as number of buildings in the
direct surroundings; 2) the distribution of these trips to destinations
depends on explicitly geographic factors such as absolute and relative
distances; 3) mode split is influenced by geographic factors such as the
gradient and motor traffic speeds and volumes associated with routes
between origins and destinations; and 4) assignment to the route network
clearly depends on a realistic representation of footways, cycleways,
highways and other geographic entities such as traffic lights that
affect route choice. Likewise statistical modelling includes
consideration of trip distances and destinations, which imply some level
of geographic analysis. Four-stage and statistical modelling options can
be supplemented by **geographic analysis and modelling**, something that
has been recognised since at least the 1990s (Anderson 1991). Critical
to any modelling exercise are scenarios, which can be either ‘global’
(such as a nationwide increase in fueld tax) or ‘local’ (such as the
creation of new public transport routes on specific roads) in nature.
The latter type of scenario require geographical inputs, such as
simulating a new cycleway or bus stop. These are arguably more tangible
and relevant to the city and regional levels at which many transport
plans are developed than abstract ‘global’ changes (e.g. Larsen,
Patterson, and El-Geneidy 2013).

Geographic considerations are particularly important in stage 4,
**evaluation of solutions and recommendations** to policy makers, but
are often overlooked. If recommendations resulting from an ‘optimal’
model have geographically uneven impacts, it risks exacerbating existing
spatial inequalities. Geographic analysis of the results of the
transport planning process, in addition to geographic analyis of input
data, can support more spatially equitable development which could have
a co-benefit of reducing travel demand: wage and other differences
between cities are a major driver of (often energy intensive) inter-city
travel demand. And of course the the implementation of effective
solutions relies on results that are specific, including being
geographically specific and presented in clear and accurate geographic
visualisations (Pensa, Masala, and Lami 2013). <!-- Todo: add refs -->

The stages represented in Figure <a href="#fig:schematic">1</a> have
been criticized for being simplistic, linear and ‘top-down’, with
particularly strong criticisms focusing on the lack of stages for impact
assessment and public participation (Löfgren, Nilsson, and Johansson
2018; Tornberg and Odhage 2018), and more sophisticated representations
of key stages in the planning system have been expounded for some time
(Batty 1995). However, there is little doubt that the ‘formulate →
collect → model → evaluate → implement’ approach continues to be popular
and that, within this framework, each stage (particularly ‘modelling’
which includes geographic analysis and modelling) could benefit from
increased access to geographic insights.
<!-- --- derived from geographic data and geographic analysis tools --- in support of 21^st^ Century policy drivers. -->
Due partly to data and computing limitations (outlined in the next
section) geographic considerations are not always considered, with
consequences for the solutions resulting from the transport planning
process and the extent to which they adapt to local geographic factors.
Lack of access to, knowledge of and skills in the use of tools for
geographic analysis represent another reason why geographic factors may
be excluded from transport plans (although evidence of the tools that
transport planners use and can use is scarce, suggesting areas of future
research, as discussed in Section <a href="#conclusion">6</a>). There
*is* evidence that these ‘barriers to entry’ for geographic analysis —
at high resolution based on high quality data and high performance
software — are being removed, as outlined in Section
<a href="#open-source-tools">4</a>. In this context, the aim of this
paper is to explore emerging open source tools for geographic analysis
in transport planning, with reference to the literature.
<!-- , with a focus on geographic data analysis, routing and route network analysis.
todo: include this at the end -->

<!-- The paper is structured as follows... -->

The increased availability of open access geographic data and high
performance computing technologies (in addition to policy drivers
increasing demand for geographic analysis) over the last few decades is
discussed in the next section. Despite the increasing availability of
open source options, proprietary tools still appear to dominate
transport planning in practice, as we will see in Section
<a href="#the-current-landscape">3</a>. The nature and functionality of
open source tools for geographic analysis in transport planning is
outlined in Section <a href="#open-source-tools">4</a>. Section
<a href="#conclusion">6</a> concludes by summarising the state and
future prospects of open tools in transport planning, highlighting gaps
in the current crop of open source options, and flagging ways of getting
involved to improve the provision of open source tools for the benefit
of researchers, companies, governments and interested citizens with
stakes in transport planning processes.

<!-- Transport planning documents often contain maps only for the *proposed intervention*, omitting important geographic data (and analysis) showing the geographic factors that were considered during and influenced the final design. -->

<!-- To pick one prominent example... -->

<!-- Perhaps in response to an upsurge in the amount of geographic transport data available, interest in geographic analysis in transport planning journals seems to have grown over the last decade. -->

<!-- relative to other terms, according to data obtained using the **gtrendsR** package [@massicotte_gtrendsr_2019] from Google Trends (Figure 1). -->

<!-- It is interesting to compare this growth with relative levels of interest in 'geographic information systems' and 'spatial planning', both of which seem to have seen relative declines over time, notwithstanding the limitations associated with search data [@mellon_internet_2014].  -->

<!-- The growing research interest in the subject is also reflected in teaching. -->

<!-- Modules dedicated to Transport Geography have been advertised at the Universities of Aberdeen and Hofstra and, at the University of Leeds the Masters module Sustainable Spatial Planning and Analysis ([SSPA](https://github.com/ITSLeeds/SSPA)) is focussed on GIS skills for transport planning (declaration of interest: I teach on this module), and there are even dedicated 3 year degrees Transport Geography. -->

<!-- , in relation to the history of geographic thinking in transport research and practice (in Section 3) and the resulting specialisation and monopolisation of particular transport planning software products (outlined in Section 4). -->

<!-- The focus of the paper is Section 4, which reviews open source software ecosystems that enable an integrated approach, which combines non geographically explicit stages (e.g. modelling) and geographic processing stages *in a single workflow*. -->

<!-- Three software ecosystems are reviewed in detail: -->

<!-- the statistical programming language R [@rcoreteam_language_2019], -->

<!-- the general purpose programming language Python [@rossum_python_1995], -->

<!-- and the desktop GIS QGIS [@qgisdevelopmentteam_qgis_2019]. -->

<!-- Alternative current and potential future approaches, including 'cloud lock in' are discussed; and the relative merits of different approaches are discussed. -->

<!-- Building on this discussion, Section 6 concludes by returning to the importance of integrating geographic analysis in transport planning workflows. -->

<!-- Before proceeding with the main task of this paper --- to review new tools for integrating geographic analysis in transport planning, and provide guidance to transport researchers and practitioners tackling 21^st^ Century challenges --- it is worth taking a step back, to think about the key policy drivers of 21^st^ century transport planning. -->

<!-- and outlines concrete steps that can be taken to accelerate the transition to open source software in transport planning in support of policies that accelerate the transition away from fossil fuels. -->

# Policy and technological drivers

<!-- for geographic analysis in transport planning -->

Two major drivers of change in transport planning tools have
historically been technological development and shifting political
priorities (Boyce and Williams 2015) and each of these have emphasised
the importance of geographic analysis in recent years. Environmental,
health and equality regulations — which can be seen as a manifestation
of political change — have also influenced transport planning practice
and some specific transport planning tools have emerged to tackle
particular issues (e.g. Vandenbulcke et al. 2009). Environmental
concerns, including fears about the impact of climate change, have risen
up policy agendas in recent years, meaning that such environmental
policy drivers a likely to become more important in the coming years. In
parallel, the ‘obesity crisis’ and mounting evidence of the health
benefits of physical activity have provided impetus to plans that
prioritise walking and cycling, with environmental co-benefits. There
have also been calls for more ‘bottom-up’ and participatory (implying
open source) approaches, although transport planning practice has been
slow to change in this direction (Legacy 2016). No less important is the
demand for localised results; while a national transport model can
provide a high level overview of the transport system for policy-makers,
tools that provide geographically specific results, potentially down to
the street level, can support transport planners ‘on the ground’. These
two factors drive demand for transport planning tools that are both open
and enable geographic analysis. A final driver of demand for such tools
is technology. Rapidly emerging digital technologies could transform
transport planning, with two-way communications between planning
authorities and citizens, and even peer-to-peer communications on
transport planning issues, now feasible.\[2\] Consideration of each of
these drivers of change in transport planning tools provides the context
in which incumbent and new open source tools will be assessed.

## Political drivers

The history of transport modelling shows that transport planning
software was originally designed to plan for “increased use of cars
\[for personal travel\], and trucks for deliveries and goods movement”
(Boyce and Williams 2015). Despite the fact that policy drivers have
changed dramatically — with climate change mitigation, air quality
improvement and public health prioritised in the ‘sustainable mobility
paradigm’ (Hickman, Ashiru, and Banister 2011) — incumbent transport
software still largely based on tools focussed on motor traffic,
emphasising travel time savings and (de)congestion effects of
interventions at relatively low levels of geographic resolution that may
be insufficient to map the relatively intricate details needed to
effectively design for active transport (Parkin 2018).

<!-- Todo: define 'tool' vs software vs ecosystem -->

Tools for 21<sup>st</sup> Century transport planning need to tackle very
different questions, such as: What are the barriers preventing people
from switching to more sustainable modes of transport, and where are
these barriers located? How are transport behaviours likely to shift in
the future, in response to technological changes including autonomous
vehicles and the continued rise of online working? Where will different
types of intervention be most effective? And how can citizens be engaged
in transport decisions? Tools that can help answer these questions are
becoming an increasingly important part of the transport planner’s
cabinet (te Brömmelstroet and Bertolini 2008).

As the gap between what the science seems to say is necessary in the
near future and the reality of polluting and unhealthy transport systems
grows, so does the need for transparent models that stand up to scrutiny
and enable participation and informed debate. This has been well
documented in with respect to energy models by Morrison (2018), who
observed that “opaque policy models simply engender distrust”. The same
could be said of transport models, driving demand for tools that are
open to public scrutiny and community involvement. In parallel, growing
awareness of the need for sustainable transport planning solutions has
also driven demand for geographically locallised transport planning
tools.

## Demand for localised results

With the emphasis shifting to reducing travel by building ‘liveable’
communities and enabling mode shift (Sallis et al. 2016), localised and
geographically specific considerations may become increasingly prominent
in future plans. To illustrate this point, imagine being the mayor of a
major city that has declared a ‘climate emergency’ and who has been
given the task of leading the transition away from fossil fuels
(Hadfield and Cook 2019). Policies such as carbon taxes would
undoubtedly be needed at the national level but your focus would
naturally be on the bounds of the local authority over which you have
some power.
<!-- have geographic implications, but the intervention itself (charging a fixed price for the extraction and sale of atmosphere polluting substances) could be essentially non-geographic. -->
Except for specific national transport policies such as fuel tax,
transport policies tend to have geographic outcomes (to build new cycle
infrastructure, for example, which must go somewhere) and this is
especially so for low-carbon transport plans which tend to operate over
distances of hundreds of metres rather than dozens of kilometres, due to
inherent limits in the speeds of active modes (Iacono, Krizek, and
El-Geneidy 2010).

Even high level national plans for a walking and cycling revolution must
be implemented locally, down to the level of streets, as illustrated by
the still ongoing local implementation of Dutch cycling ambitions
(Pucher and Buehler 2008). The political-democratic and local-geographic
aspects of transport planning can be considered in isolation, but an
integrated approach is necessary for effective policies (Hull 2008).
This is well illustrated by prominent Mayoral transport policies in
cities such as London,\[3\] Paris\[4\], and Bogotá,\[5\] where
geographically specific interventions (such as congestion charges in
carefully demarcated central zones) combined with citywide vision have
enabled modal shift.

With issues such as climate change, air pollution, obesity and social
inequalities high on the political agenda, and the benefits for ‘early
adopters’ of evidence-based interventions to accelerate the shift away
from the motor car in cities such as London, Paris and Bogotá, pressure
is growing on local, city and national transport planning departments to
act. But what should they do, and where should they intervene?
Geographical data and to some extent analysis (e.g. calculating
distances) was integral to this ‘computational transport planning’
activity, but input datasets were limited in size and accuracy. Partly
in response to such drivers for geographic analysis in transport
planning, there have been various attempts to define a more applied GIS
approach transport research. Miller (1999) advocated a new field, GIS
for Transport (GIS-T), posited as an academic field at the interface
between transport planning and GIS. Although the label gained limited
traction in academia or practice, Harvey Miller’s call for a shift to
methods and tools has been answered in the 2000s and 2010s by
researchers who have developed ideas and software that transport
planners can actually use, including the Australian Research
Infrastructure Network (AURIN), which is widely used for transport
planning and public health research in Australia (Pettit et al. 2014)
and the Propensity to Cycle Tool (PCT, publicly available, including
source code, at [www.pct.bike](https://www.pct.bike)) (Goodman et al.
2019). <!-- refs? -->

## Technological drivers

Technological change has increased the capabilities of transport
planners since the the beginning of the discipline, with transport
planning tasks being an early use case of mainframe computers (Boyce and
Williams 2015). With unprecedented access to increasingly detailed
datasets on transport behaviours and infrastructure, transport planners
today require tools that enable them to make sense of this ‘data
revolution’ (Transport Systems Catapult 2015). The sheer volume and
complexity of new datasets require new approaches that can scale and
integrate multiple data sources (Lovelace et al. 2016). Advances in
software and hardware allow not only for current transport systems to be
modelled at high temporal and geographic resolution, but for future
scenarios and ‘model experiments’ to be developed, which can support
identification and implementation of the most effective interventions
(Klosterman 1999).

With the explosion in open source software, which has come to dominate
data science, policy, data and technological drivers are pushing for
geographic analysis to be better integrated in transport planning tools,
alongside wider shifts for towards more data driven, transparent and
democratically accountable transport planning workflows. At present this
dream is far from reality, despite the long history of geographic
methods, public involvement and technological innovation in transport
planning.

<!-- This *policy* question raises important *research* questions: -->

<!-- Which methods are most suitable for designing future transport systems? -->

<!-- What is the evidence base, and analysis, that should be used to inform transition towards a healthy, zero carbon transport system? -->

<!-- Which interventions, from the multitude of options available, are most likely to be effective? -->

<!-- And where are different types of intervention most likely to succeed? -->

<!-- The premise of this paper is that new approaches, enabled by software, are needed to provide answers to these questions. -->

<!-- 21^st^ Century demands for transport planning cannot be delivered by 20^th^ century technology. -->

<!-- Could open source solutions are poised to bridge the gap between the geographic and the --- historically dominant --- non-geographic aspects of transport planning? -->

<!-- Planning for sustainable modes, walking and cycling in particular, requires analysis at higher geographic resolutions than planning for motor traffic. -->

<!-- Furthermore, the policy context increasingly demands transparency and citizen involvement in the decision-making process. -->

<!-- Only open source ecosystems, of the type outlined in Section <a href="#new-tools-of-the-trade"><strong>??</strong></a> can deliver true transparency and encourage 'citizen science' for everyone. -->

<!-- These policy drivers make an exploration of open source options for transport planning workflows timely. -->

<!-- Additional drivers of change in transport planning software include new datasets and technologies. -->

<!-- Technological change has historically driven innovation in transport planning tools [@boyce_forecasting_2015] and the rate of change now is faster than ever. -->

<!-- In the inter-war period (1918-1939) disciplinary homes for transport research had yet to emerge and geographic analysis was limited by lack of datasets and computers on which to process them. -->

<!-- The term 'transport geography' itself only became widespread in the 1950s: -->

<!-- as noted in a report commissioned by the US Office of Naval Research: -->

<!-- "geographers, both in Europe and America, are coming to recognize that the study of the connections between areas and of spatial interchange can provide a new and deeper insight into the meaning of areal differentiation" [@ullman_transportation_1954].  -->

<!-- In the pre-computing age the relationship between geographic analysis and transport planning was characterised by growing interest in the topic, an understanding of the importance of geographic considerations in the design and evolution of transport systems, but lack of data and computational resources.^[ -->

<!-- @paterson_horse_1926, for example, speculated quite accurately on the continued rise of motor traffic at the expense of horse powered transport during the 20^th^ Century, noting the importance of geographic factors in determining mode choice, down to the street level: -->

<!-- "Many streets, like our Bond Street, Watling Street or Lombard Street, and in Seville, the Calle de las Sierpes or Kalver Straat in Amsterdam, may be unsuited to motor traffic, and frontage values may be so high that widening can hardly be considered." -->

<!-- In a geographic review of Japanese cities @trewartha_japanese_1934 also alluded to the relationship between geography and mode choice: -->

<!-- "widening and paving of [roads] have (sic) been accomplished [allowing] numerous taxis, motor busses, and tram cars contrasting with the slow human and animal-drawn carts and the ubiquitous bicycle". -->

<!-- Rapid industrialisation during the largely unconscious build-up to World War II was associated with major road building schemes in many developed regions, demanding the practical application of new methods from a range of disciplines [e.g. @greenshields_studying_1936]. -->

<!-- In the USA, highway engineering even became a recommended case study for geography lessons [@fox_main_1923]. -->

<!-- ] -->

<!-- At the turn of the computing age in the 1950s and 1960s transport planners, whose primary task was often to enable rapid growth in car ownership and use, quickly saw the potential for computational tools to assist their work [@boyce_forecasting_2015]: "essential to [new methods in transport planning] were new computational capabilities, the first mainframe computers, unprecedented in memory and speed [yet] tiny from today’s perspective". -->

<!-- As *Forecasting Urban Travel* [@boyce_forecasting_2015] recounts, geographic questions were at the forefront of many planners' minds and a key task for the early transport models was to visualise and model the results of large origin-destination surveys to help decide where new highways should be constructed. -->

<!-- Much of the early work in this field was publicly funded and focussed on solving real world problems associated with population growth, economic development, changes in lifestyles, and mobility behaviours. -->

<!-- However academics, and quantitative geographers in particular, soon started working with newly available transport datasets. -->

<!-- An important development was the emergence of spatial interaction models, which were formally defined, refined and implemented throughout the 1960s and 1970s [@wilson_statistical_1967; @wilson_family_1971]. -->

<!-- It is notable that Alan Wilson, whose research influenced both transport planning and academic practice, worked in both the public sector (for the UK's Ministry of Transport) and academia (the University of Leeds) while writing each paper. -->

<!-- Most academic research at the interface between transport planning and geographic research is far less 'practitioner facing' and, if anything, it seems that tools used in geographic analysis of transport systems in practice since the 1970s have diverged from academic research. -->

<!-- perhaps explaining why the field of Transport Geography, which emerged in the 1960s and grew rapidly since then [@hay_transport_1979], has (to the author's knowledge) had relatively few other notable impacts on transport planning practice. -->

<!-- By the late 1970s, there was enough research for review papers reflecting on the status of Transport Geography as a self-standing branch of Geography [@rimmer_redirections_1978]. -->

<!-- A book on the transport geography of India provides an insight into the field at the time, with a focus on infrastructure and statistics, transport geography sat firmly in the quantitative tradition of geographic research [@raza_transport_1986], despite Rimmer (1979) criticism that much of the field ignored the wider impacts of transport systems. -->

<!-- Geographic analysis in transport research was given a substantial boost in the 1990s, with the first publication of the Journal of Transport Geography [@knowles_research_1993]. -->

<!-- Transport Geography has subsequently come to be defined as a branch of geography. -->

<!-- Notwithstanding influential methodological and review papers proving transport planners with insight into the state-of-the-art [e.g. @martinez_new_2013], the level of engagement between academic transport geographers and transport planning practitioners is debatable (although the same could also be said of academic planners).  -->

<!-- Search term for interwar period: https://scholar.google.co.uk/scholar?q="transport+geography" -->

<!-- something on the lack of open source? -->

<!-- https://www.abdn.ac.uk/registry/courses/undergraduate/2016-2017/geography/gg4016
https://people.hofstra.edu/jean-paul_rodrigue/course_transport.html
 in Geography with Transport Studies BA advertised by the University of Leeds
-->

<!-- Transport planning has been slow to adapt to the data revolution and, while it evolves to enable a wider range of input data sources and analysis 'in the cloud', the open source element is conspicuously lacking. -->

<!-- To understand and effectively challenge the incumbent software landscape (which is described in Section xx) it is worth understanding something of the history that led to this situation. -->

<!-- # Geographic analysis and transport planning -->

<!-- The concept of integrating geographic data analysis in transport planning is not new, although tools and datasets for doing so quantitatively are. -->

<!-- Geographic perspectives have contributed to transport thinking for over 100 years, as documented in papers on geographic considerations in railway design and other transport engineering challenges [@farnham_relation_1912; @buxton_balkan_1908]. -->

<!-- Since then, the importance of geographic analysis in transport planning has only grown, with the realisation that interventions in the transport system are most effective when they are placed where they are most needed: infrastructure designs and localised policies are most effective when they account for the geographic distribution of intricate spatial networks and interacting places of transport supply and demand -->

<!--  [@rodrigue_geography_2013; @loidl_gis_2016; @lovelace_propensity_2017]. -->

<!-- The paper concludes that 'integrated approach' can support efficient, scalable and reproducible transport planning workflows which can provide a strong and transparent evidence base needed for rapid transition away from fossil fuels in the transport sector. -->

# The current landscape

In broad terms, digital transport planning tools are like any other
computer program in that they take inputs which are processed to
generate outputs (Knuth 1997). The broader term ‘transport model’ is
sometimes used interchangeably with transport software but in this paper
we follow (Hollander 2016) in using ‘model’ to refer to the theories and
mathematics underlying transport planning software, rather than the
software that implements the model.\[6\] In relation to the narrower
concept of ‘algorithm’, transport planning software can be seen as a
computing environment or system that provides a user interface to run a
range of algorithms interactively on a range of input datasets to
generate outputs that can feed into the wider transport planning process
(Boyce and Williams 2015).

Software for transport planning can be grouped by the scale at which it
operates, with broad categories being microscopic and macroscopic
(macro) models (Kotusevski and Hawick 2009; Hildebrand and Hörtin 2014).
Microscopic transport models represent individual vehicles on the road
network and are therefore able to represent localised phenomena such as
traffic congestion. Macro models, by contrast, represent aggregates of
vehicular traffic over large spatial scales, in which “the total flow is
studied” and behaviour of individual vehicles is omitted (Hildebrand and
Hörtin 2014). Of course the distinction is, in reality, an
oversimplification: there is a continuum between macro and microscopic
transport models; advances in computing increasingly enable both
approaches to be combined, enabling researchers to choose the most
appropriate spatial scales for their application (Moeckel et al. 2018).
The focus of this paper is on macro models which enable modelling of the
implications of future changes in transport behaviour and infrastructure
on flow at city scales, with results down the route network level
(microscopic models tend to be used to model individual route segments
and intersections), and their geographic analysis capabilities.

<!-- The geographic and non-geographic division of labour is a result of the history of transport planning software. -->

This history is detailed in Chapter 10 of *Forecasting Urban Travel*
(Boyce and Williams 2015) called “Computing environment and travel
forecasting software”, which provides an insight into how software has
been used in transport planning over the years. Of course, software
development has always depended on the physical hardware on which it
runs and the early days of transport planning software were
characterised by bespoke programs running on mainframe computers and
maintained by domain experts. Transport planning bodies and researchers
in the USA led developments in the 1960s and 1970s when computers first
started to be used for transport planning, when the main problem that
they addressed was how to deal with the explosive growth in car
ownership and use that was taking place during those decades. More
overtly political factors also influenced the direction of transport
planning software: “certain private firms complained to US DoT
\[Department of Transport\] that its agencies were developing software
in competition with the private sector”, leading to the abandonment of
publicly funded transport planning software development projects,
notably UTPS (Boyce and Williams 2015).\[7\] This transfer of transport
planning software development to the private sector contrasts with the
history of GIS. The example of GRASS (Geographic Resources Analysis
Support System) illustrates this point and helps explain the dominance
of proprietary software in transport planning. Like UTPS, GRASS was a
publicly funded software project. Unlike UTPS, it was made freely
available to the public and was open sourced (in 1999), meaning that it
has been under continuous development by state, academic and commercial
organisation since 1982 (Neteler and Mitasova 2008). Would the landscape
of transport planning software have been different if the DoT had
continued to fund software development projects? That question is
outside the scope of this paper. What is certain, however, is that
software used in transport planning over the past three decades has been
dominated by companies and that the sector has been slow to adopt open
an open source approach.

In response to the ‘siloed’ development of GIS and transport software,
there have been calls for greater integration. Loidl et al. (2016),
building on the observation that “geography and GIS remained a niche
topic within traditional transport modeling”, made a case for
strengthening the ‘spatial perspective’ in transport modelling. The
paper emphasised the growing importance of well-defined data types,
disaggregating detailed (and difficult to interpret) transport model
outputs, and geographic data visualisation and concluded that much
further research is needed: “future research and development is needed
to combine geospatial functionalities with transport modeling, while
providing an efficient, interactive, visual interface for data
exploration, manipulation, analysis and visualization” (Loidl et al.
2016). Although the paper focussed on conceptual issues rather than
software per-se, it did identify mention four open source programming
languages that could provide the foundation for future developments, two
of which (R and Python) are covered in the next section.

Data preprocessing and analysis stages are generally done in dedicated
transport planning and spreadsheet software. Geographic analysis and
cartographic visualisation stages are often done in a dedicated GIS.
Some prominent transport planning software products, and levels of
support for geographic data analysis, are summarised in Table 1, which
shows that popular transport planning tools have differing levels of
geographic capabilities.

| Software | Company/Developer  | Licence           | I | G | R | RNA | SV | IV | EX |
| :------- | :----------------- | :---------------- | :- | :- | :- | :-- | :- | :- | :- |
| Visum    | PTV                | Proprietary       | Y | Y | Y | Y   | Y  | ?  | ?  |
| MATSim   | TU Berlin          | Open source (GPL) | Y | ? | Y | Y   | Y  | ?  | ?  |
| TransCAD | Caliper            | Proprietary       | Y | Y | Y | Y   | Y  | ?  | ?  |
| SUMO     | DLR                | Open source (EPL) | Y | ? | ? | Y   | Y  | ?  | ?  |
| Emme     | INRO               | Proprietary       | Y | Y | Y | Y   | Y  | ?  | Y  |
| Cube     | Citilabs           | Proprietary       | Y | ? | ? | Y   | Y  | ?  | ?  |
| sDNA     | Cardiff University | Open source (GPL) | Y | Y | Y | Y   | ?  | ?  | ?  |

Table 1: Sample of transport modelling software in use by practitioners,
with citation counts based on citation from searches for
company/developer name, the product name and ‘transport’. The columns I,
G, R, RNA, SV, IV and EX refer to Import of a wide range of geographic
data formats, Geographic capabilities such as buffer calculations and
intersections, Route calculation, Route Network Analysis, Static Visual
outputs, Interactive Visual outputs for web publication, and Export to a
wide range of geographic data formats, with ? meaning partial support
(e.g. via add-on software). Data source: Google Scholar searches,
October 2018.

<!-- The geographic capabilities were assessed based on reading of publicly available manuals (to be linked to in an appendix accompanying this paper) and that each software product is actively developed, meaning that the results may change with additional information and subsequent releases. -->

An interesting observation is that the open source options — MATSim,
SUMO and sDNA — all have limited ‘in house’ geographic capabilities.
This can be explained by the ‘Unix philosophy’, the second tenet of
which is modularity, meaning that “each program should do one thing
well”, reducing duplication of effort and allowing the best tool to be
used for each job (Gancarz 2003). The next section describes the this
modularity in more detail, including outstanding support for geographic
data in open source software.

A major barrier affecting the current landscape of transport planning
tools is accessibility and reproducibility: all the proprietary products
are expensive (costing hundreds of dollars for a single license),
ensuring that only a small fraction of transport planners, let alone the
public, has access to them. Another barrier associated with the
proprietary options is platform dependence: as far as the author can
tell, they all run only on the proprietary operating system Windows,
preventing use in on other operating systems such as Linux, Mac and
FreeBSD. A final issue affecting reproducibility with the proprietary
options listed in Table 1 is that they all have a prominent Graphical
User Interface (GUI) (although they increasingly offer a command line
interface, enabling scripting). As is the case with GUI based GIS
software, this has the “unintended consequence of discouraging
reproducibility” by enabling the user to get to a solution without
writing a script that others can use (Lovelace, Nowosad, and Meunchow
2019).

Another barrier, which may affect the open source options listed in
Table 1 more than the proprietary options, is that they can be (in the
author’s experience) difficult to install and use. This creates an
additional barrier to the integration of geographic analysis in
transport planning for people, especially the majority of people who
have limited computing skills.

A final barrier, which may be more social and organisational than
software-related (although discerning cause and effect is difficult), is
that organisations’ GIS and Transport functions tend to be siloed into
their respective departments/teams with little communication between
them, meaning that transport planners may not have access to the latest
geographic data or software.\[8\] A software-related issue is that, if
transport planners and GIS analysts are using different programs for
their work, transport planners will be less likely to collaborate with
people with geographic analysis skills or identify potential geographic
solutions to their domain-specific problems. To what extent can these
barriers be overcome by open source software ecosystems? That is the
topic of the next section.

<!-- @kammeier_new_1999 -->

# Open source tools for geographic analysis in transport planning

<!-- The previous sections support and expand on the two main premises of this paper: that geographic analysis has much to offer transport planning, and that the incumbent proprietary software products are not well suited to tackle 21^st^ Century transport planning needs. -->

<!-- In this section the paper shifts gear, and moves onto solutions. -->

The previous sections suggest that technological, environment and
societal changes are driving demand for geographic analysis via
accessible tools in transport planning. This section reviews prominent
open source tools that could, and in some cases already are, being used
to tackle research, and increasingly applied, transport planning
challenges. Open source tools for geographic analysis in transport
planning have not emerged in a vacuum. They were developed in the wider
landscape of open source software (Dhir and Dhir 2017).

These tools could be classified by the five main stages illustrated in
Figure <a href="#fig:schematic">1</a> (data collection, processing,
routing, modelling and visualisation). Instead, because many tools can
be used in multiple stages, can be more usefully classified from the
user’s perspective. Based on open tools identified through web searches,
they can be classified into the follow broad, and to some extent
overlapping,\[9\] user interface (UI) types (see Table
<a href="#tab:open-tools">2</a>):

  - command-line interface (CLI) tools, primarily controlled by typing
    commands
  - graphical user interface (GUI) tools, primarily controlled by mouse
    clicks
  - web user interface (WUI) tools that users access through a web
    browser

## Defining open source

Before describing open source tools for transport planning, classified
by their main user interface, is worth considering what ‘open source’
means.
<!-- and how the people, organisations and communities developing these technologies work; this to provide pointers for readers interested in contributing to open source transport planning software projects (more on this in the final section). -->

<!-- Despite the central role that open source software plays, powering the majority of the world's servers... -->

Open source software differs from proprietary software in that users are
free to see, download and modify the source code. Freedom is central to
open source software, which is sometimes referred to simply as ‘free
software’, defined by the Free Software Foundation (FSF) as
follows:\[10\]

> software that gives you the user the freedom to share, study and
> modify it.

This adaptability is conducive to collaboration, the creation of
mutually supportive user/developer communities and rapid evolution,
making open source software ecosystems fast moving and highly diverse.
It is impossible to discuss all software options that could be used for
geographic transport planning: there are literally thousands of software
projects written in dozens of programming languages, many of which are
no longer actively maintained (Coelho et al. 2020). Transport planners
should use solutions that are future proof and actively maintained.

## Methods to identify open source tools

To identify open source tools for transport planning, a search approach
was used to incorporate projects that have been written-up in the
academic literature, and projects which exist only as software projects,
with a minimum level of popularity. The method was as follows:

1.  Undertake searches of Google Scholar, DuckDuckGo and the popular
    code hosting platform with search terms set to identify open source
    projects.
2.  Combine results from the searches into a single dataset and rank the
    projects according to evidence of usage.
3.  Verify that the projects are open source and actively maintained by
    analysis of package documentation and source code.
4.  Classify and the projects based on their main user interface,
    resulting in the top 10 open source tools for geographic analysis in
    transport planning shown in Table <a href="#tab:open-tools">2</a>
    (see the appendix for a complete table of results). These tools are
    described in more detail in the following three sections.

The following search terms were used to find relevant projects using
Google Scholar, the result of a search shown in Figure
<a href="#fig:scholar-search">2</a>:

<!-- > "open source" software "transport planning" "geographic data" OR "geographic analysis" OR "spatial data" OR spatial OR analysis" -->

> software transport “open source” “transport planning” OR “geographic
> data” OR “geographic analysis” OR “spatial data” OR “spatial network”

To identify open source projects on GitHub an alternative approach was
taken due to the limited capabilities of GitHub’s [advanced search
page](https://github.com/search/advanced): An ‘snowball’ method,
analogous to that used by Grabowicz et al. (2012) in the context of
social media, was used whereby known projects were identified and the
‘topic’ descriptions they used were searched for to identify
additional projects and search terms. This method worked as follows:

<div class="figure">

<img src="scholar-search.png" alt="Illustration of the Google Scholar search terms used to identify open source software for geographic analysis in transport planning." width="60%" />

<p class="caption">

Figure 2: Illustration of the Google Scholar search terms used to
identify open source software for geographic analysis in transport
planning.

</p>

</div>

  - The search term [`transport
    planning`](https://github.com/search?q=transport+planning&type=Repositories&l=&l=)
    identified the stplanr project.
  - One of the ‘topics’ in the stplanr repository was was the broader
    term `transport`, which was used to identify the SUMO projct
  - The SUMO project also had the term ‘simulation’, leading to the
    discovery of the abstreet project

The complete list of GitHub topics used to identify projects was as
follows (manual reading of the README for each project was used to
confirm if the projects were related to transport planning, many were
not, e.g. because they were for web transport rather than transport
planning):

> [transport planning](https://github.com/topics/transport-planning),
> [transport](https://github.com/topics/transport),
> [transportation-planning](https://github.com/topics/transportation-planning),
> [traffic-simulation](https://github.com/topics/traffic-simulation),
> [simulation](https://github.com/topics/simulation),
> [trajectory](https://github.com/topics/trajectory)

<table>

<caption>

Table 2: Open source tools for geographic analysis in transport
planning, based on data from Google Scholar, GitHub and web searches and
classified in by their primary user interface. CLI, GUI and WUI refer to
command-line, graphical user and web user interfaces respectively.

</caption>

<thead>

<tr>

<th style="text-align:left;">

Tool

</th>

<th style="text-align:left;">

Type

</th>

<th style="text-align:left;">

Licence

</th>

<th style="text-align:left;">

Langage

</th>

<th style="text-align:right;">

Stars

</th>

<th style="text-align:right;">

Citations

</th>

<th style="text-align:left;">

Reference

</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:left;">

OSMnx

</td>

<td style="text-align:left;">

Python package

</td>

<td style="text-align:left;">

MIT

</td>

<td style="text-align:left;">

Python

</td>

<td style="text-align:right;">

2496

</td>

<td style="text-align:right;">

302

</td>

<td style="text-align:left;">

(Boeing 2017)

</td>

</tr>

<tr>

<td style="text-align:left;">

SUMO

</td>

<td style="text-align:left;">

Standalone

</td>

<td style="text-align:left;">

EPL-2.0

</td>

<td style="text-align:left;">

C++

</td>

<td style="text-align:right;">

736

</td>

<td style="text-align:right;">

219

</td>

<td style="text-align:left;">

(Lopez et al. 2018)

</td>

</tr>

<tr>

<td style="text-align:left;">

MovingPandas

</td>

<td style="text-align:left;">

Python package

</td>

<td style="text-align:left;">

BSD-3

</td>

<td style="text-align:left;">

Python

</td>

<td style="text-align:right;">

307

</td>

<td style="text-align:right;">

6

</td>

<td style="text-align:left;">

(Graser 2019)

</td>

</tr>

<tr>

<td style="text-align:left;">

MATSim

</td>

<td style="text-align:left;">

Standalone

</td>

<td style="text-align:left;">

GPLv2

</td>

<td style="text-align:left;">

Java

</td>

<td style="text-align:right;">

285

</td>

<td style="text-align:right;">

564

</td>

<td style="text-align:left;">

(Horni et al. 2016)

</td>

</tr>

<tr>

<td style="text-align:left;">

Scikit-mobility

</td>

<td style="text-align:left;">

Python package

</td>

<td style="text-align:left;">

BSD-3

</td>

<td style="text-align:left;">

Python

</td>

<td style="text-align:right;">

251

</td>

<td style="text-align:right;">

1

</td>

<td style="text-align:left;">

(Pappalardo et al. 2019)

</td>

</tr>

<tr>

<td style="text-align:left;">

stplanr

</td>

<td style="text-align:left;">

R package

</td>

<td style="text-align:left;">

MIT

</td>

<td style="text-align:left;">

R

</td>

<td style="text-align:right;">

201

</td>

<td style="text-align:right;">

9

</td>

<td style="text-align:left;">

(Lovelace et al. 2018)

</td>

</tr>

<tr>

<td style="text-align:left;">

momepy

</td>

<td style="text-align:left;">

Python package

</td>

<td style="text-align:left;">

MIT

</td>

<td style="text-align:left;">

Python

</td>

<td style="text-align:right;">

133

</td>

<td style="text-align:right;">

3

</td>

<td style="text-align:left;">

(Fleischmann 2019)

</td>

</tr>

<tr>

<td style="text-align:left;">

Trip-simulator

</td>

<td style="text-align:left;">

JavaScript package

</td>

<td style="text-align:left;">

MIT

</td>

<td style="text-align:left;">

JavaScript

</td>

<td style="text-align:right;">

117

</td>

<td style="text-align:right;">

NA

</td>

<td style="text-align:left;">

NA

</td>

</tr>

<tr>

<td style="text-align:left;">

urbanaccess

</td>

<td style="text-align:left;">

Python package

</td>

<td style="text-align:left;">

AGPLv3

</td>

<td style="text-align:left;">

Python

</td>

<td style="text-align:right;">

105

</td>

<td style="text-align:right;">

12

</td>

<td style="text-align:left;">

(Blanchard 2017)

</td>

</tr>

<tr>

<td style="text-align:left;">

dodgr

</td>

<td style="text-align:left;">

R package

</td>

<td style="text-align:left;">

GPLv3

</td>

<td style="text-align:left;">

C++

</td>

<td style="text-align:right;">

84

</td>

<td style="text-align:right;">

2

</td>

<td style="text-align:left;">

NA

</td>

</tr>

<tr>

<td style="text-align:left;">

spaghetti

</td>

<td style="text-align:left;">

Python package

</td>

<td style="text-align:left;">

BSD-3

</td>

<td style="text-align:left;">

Python

</td>

<td style="text-align:right;">

60

</td>

<td style="text-align:right;">

0

</td>

<td style="text-align:left;">

NA

</td>

</tr>

<tr>

<td style="text-align:left;">

optentripplanner

</td>

<td style="text-align:left;">

R package

</td>

<td style="text-align:left;">

GPLv3

</td>

<td style="text-align:left;">

R

</td>

<td style="text-align:right;">

47

</td>

<td style="text-align:right;">

0

</td>

<td style="text-align:left;">

(Morgan et al. 2019)

</td>

</tr>

<tr>

<td style="text-align:left;">

abstreet

</td>

<td style="text-align:left;">

Standalone

</td>

<td style="text-align:left;">

Apache-2.0

</td>

<td style="text-align:left;">

Rust

</td>

<td style="text-align:right;">

4896

</td>

<td style="text-align:right;">

NA

</td>

<td style="text-align:left;">

NA

</td>

</tr>

<tr>

<td style="text-align:left;">

AequilibraE

</td>

<td style="text-align:left;">

QGIS plugin

</td>

<td style="text-align:left;">

Custom

</td>

<td style="text-align:left;">

Python

</td>

<td style="text-align:right;">

57

</td>

<td style="text-align:right;">

3

</td>

<td style="text-align:left;">

(Carmargo 2015)

</td>

</tr>

<tr>

<td style="text-align:left;">

ORS Tools

</td>

<td style="text-align:left;">

QGIS plugin

</td>

<td style="text-align:left;">

MIT

</td>

<td style="text-align:left;">

Python

</td>

<td style="text-align:right;">

39

</td>

<td style="text-align:right;">

NA

</td>

<td style="text-align:left;">

NA

</td>

</tr>

<tr>

<td style="text-align:left;">

QNEAT3

</td>

<td style="text-align:left;">

QGIS plugin

</td>

<td style="text-align:left;">

GPLv3

</td>

<td style="text-align:left;">

Python

</td>

<td style="text-align:right;">

35

</td>

<td style="text-align:right;">

NA

</td>

<td style="text-align:left;">

NA

</td>

</tr>

<tr>

<td style="text-align:left;">

Networks plugin

</td>

<td style="text-align:left;">

QGIS plugin

</td>

<td style="text-align:left;">

GPLv3

</td>

<td style="text-align:left;">

Python

</td>

<td style="text-align:right;">

9

</td>

<td style="text-align:right;">

NA

</td>

<td style="text-align:left;">

NA

</td>

</tr>

<tr>

<td style="text-align:left;">

sDNA

</td>

<td style="text-align:left;">

QGIS plugin

</td>

<td style="text-align:left;">

GPLv3

</td>

<td style="text-align:left;">

C++

</td>

<td style="text-align:right;">

9

</td>

<td style="text-align:right;">

27

</td>

<td style="text-align:left;">

(Cooper 2015)

</td>

</tr>

<tr>

<td style="text-align:left;">

Citybound

</td>

<td style="text-align:left;">

Standalone

</td>

<td style="text-align:left;">

AGPLv3

</td>

<td style="text-align:left;">

Rust

</td>

<td style="text-align:right;">

6124

</td>

<td style="text-align:right;">

NA

</td>

<td style="text-align:left;">

NA

</td>

</tr>

<tr>

<td style="text-align:left;">

StreetMix

</td>

<td style="text-align:left;">

Hosted service

</td>

<td style="text-align:left;">

BSD-3

</td>

<td style="text-align:left;">

JavaScript

</td>

<td style="text-align:right;">

440

</td>

<td style="text-align:right;">

6

</td>

<td style="text-align:left;">

(Riggs et al. 2016)

</td>

</tr>

<tr>

<td style="text-align:left;">

flowmap.blue

</td>

<td style="text-align:left;">

Standalone

</td>

<td style="text-align:left;">

MIT

</td>

<td style="text-align:left;">

TypeScript

</td>

<td style="text-align:right;">

90

</td>

<td style="text-align:right;">

NA

</td>

<td style="text-align:left;">

NA

</td>

</tr>

<tr>

<td style="text-align:left;">

PCT

</td>

<td style="text-align:left;">

Hosted service

</td>

<td style="text-align:left;">

AGPLv3

</td>

<td style="text-align:left;">

R

</td>

<td style="text-align:right;">

16

</td>

<td style="text-align:right;">

66

</td>

<td style="text-align:left;">

(Lovelace et al. 2017)

</td>

</tr>

<tr>

<td style="text-align:left;">

TrajAnalytics

</td>

<td style="text-align:left;">

Standalone

</td>

<td style="text-align:left;">

BSD-3

</td>

<td style="text-align:left;">

JavaScript

</td>

<td style="text-align:right;">

NA

</td>

<td style="text-align:right;">

0

</td>

<td style="text-align:left;">

(Shamal et al. 2019)

</td>

</tr>

</tbody>

</table>

Finally, to overcome the limitation that not all open source software
projects are hosted on GitHub *or* described in academic papers,
snowballing via fora such as the [QGIS plugin
homepage](https://plugins.qgis.org/) and links in project README files
were used to find additional projects that met the following criteria:

1.  The tool uses geographic analysis for transport planning, supporting
    the design and placement of physical infrastructure for urban
    mobility, based on the project’s website or code repository
2.  Evidence that the tool is being used in practice, via citations,
    ‘stars’ or other type of ‘upvote’
3.  Evidence that the tool is actively maintained, with activity in the
    last 12 months
4.  Availability of source code with a visible open source license

124 projects or papers were identified using the methods outlined using
the methods described above. Of those, 17 met the criteria listed above
(see Table <a href="#tab:open-tools">2</a>). Although these tools could
also be classified into different ‘ecosystems’, such as R packages,
Python packages and QGIS plugins, it is clear that some tools do not fit
into such prescribed boxes. We therefore describe the tools in order of
their primary user interface, in chronological order of the interface’s
development (CLIs predate GUIs which predate WUIs).

<!-- --- such as R, Python and QGIS.  -->

<!-- Each open source ecosystem, and it's potential to be used for geographic analysis in transport planning, is outlined below. -->

## Command-line interface (CLI) tools

Tools based on a *command line interface* (CLI) are designed to be
controlled primarily by typing commands. CLIs predate *graphical user
interfaces* (GUIs), which are controlled by ‘pointing and clicking’
(Sherman 2008). CLIs can take time to learn, especially for people who
have been trained on GUI-based software such as Microsoft Word. After
overcoming often steep ‘learning curves’, the advantages of CLI-based
tools for *users* become substantial. The approach can be highly
productive, with hundreds of commands only a few keystrokes away and the
benefits of reproducibility and scalability associated with representing
computational workflows in code. Programming also provides flexibility:
the user is not constrained by the options provided in the GUI and in
many CLI-based tools can define new functions. The approach also has
advantages for *developers*: it is substantially easier to write
software without the burden of having to develop a GUI, reducing the
barrier to entry for potential contributors. Ease of development
explains why CLIs represent the most common type of open source tool for
geographic analysis.
<!-- Transport data analysis has much in common with the broadly defined field of 'data science', and many of the tools developed for this purpose (including those in the R and Python ecosystems detailed in the next section) have great potential for transport planning. -->

The longest standing and still actively maintained CLI tools for
geographic analysis in transport planning shown in Table
<a href="#tab:open-tools">2</a> are **SUMO** (first released in 2001)
and **MATSim** (first released in 2006). Both projects are traffic
microsimulation models (with meso and in the cast of MATSim macroscopic
capabilities) that simulate individual vehicles at high spatial and
temporal resolution. Neither project focus on geographic analysis, but
they both rely on geographic inputs (detailed road geometries) and
produce geographic outputs.

**MATSim**, which stands for Multi-Agent Transport Simulation, is
perhaps the more ambitious project, enabling the transport systems of
entire cities to be simulated, creating opportunities for detailed model
experiments based on transport networks that can be edited using a
plugin to the [JOSM
GIS](https://github.com/matsim-org/josm-matsim-plugin) (Horni, Nagel,
and Axhausen 2016a). **SUMO** is focussed on modelling traffic on road
segments and junctions and although the emphasis is not on geographic
analysis, the inclusion of a geographic road network editor (called
NETEDIT) means that the tool can be used to analyse geographic scenarios
of change (Lopez et al. 2018).

With complex installation and usage instructions, **SUMO** and
**MATSim** are both aimed at advanced users. This has the advantage of
enabling many research and (particularly in the case of **MATSim**)
applied use cases due to the flexibility of the tools, but has the
disadvantage of reducing accessibility.

The remaining CLI-based tools in Table <a href="#tab:open-tools">2</a>
are smaller, simpler and more accessible R/Python packages that fit
within the framework of these pre-existing open source software
ecosystems. **osmnx** is a Python package for downloading and analysing
transport networks from OpenStreetMap that has a focus on urban
transport network analysis (Boeing 2017). **OSMnx** has been used for a
wide range of research and real-world applications, with a focus on
spatial network analysis via functions for calculating a range of
transport network measures. **Movingpandas** is a Python package and
QGIS plug-in for visualising a wide range of movement datasets, with a
focus on trajectory data (Graser 2019). **momepy** is a Python package
for measuring ‘urban morphology’, meaning the measurement and analysis
of collections of geographic entities that constitute cities
(Fleischmann 2019).

Python packages **UrbanAccess** and **scikit-mobility** have a broader
remit, aiming to support a range of transport planning objectives.
**UrbanAccess** is another Python package for analysing geographic
transport network data, with a focus on accessibility. The paper
describing the tool has more of a focus on applied transport planning
than other Python tools, highlighting the potential for the tool to
assist metropolitan planning organizations (MPOs) to prioritise
investments that cost-effectively increase accessibility for those most
in need (Blanchard and Waddell 2017). In addition to using OSM data,
**UrbanAccess** can import and process GTFS data to calculate
multi-modal travel times and other metrics. **scikit-mobility**
implements a framework for statistical modelling of travel behaviour,
including functions for estimating movement between geographic zones
using spatial interaction models, as well as route assignment
(Pappalardo et al. 2019a).

The remaining two CLI-based tools in Table
<a href="#tab:open-tools">2</a> are R packages focussed on applied
transport planning. **stplanr** (which stands for sustainable transport
planning with R) contains a range of functions for processing
origin-destination, routes and route networks. The package takes an
explicitly geographic approach to transport planning and many of the
functions use geographic operations such as buffers and spatial
aggregation in workflows that start with origin-destination data and end
with estimates of travel demand down to the route network level under
different scenarios of change (Lovelace and Ellison 2018a).
**opentripplanner** is an R package for multi-modal routing and
accessibility analysis that provides an interface to the OpenTripPlanner
Java library, enabling not only calculation of travel times and route
geometries but also monetary costs and accessibility isochrone maps
where GTFS data allow (Morgan et al. 2019).

## Graphical user interface (GUI) tools

## Web user interface (WUI) tools

<!-- ### The propensity to cycle tool -->

### Streetmix

# Software ecosystems

Many of the tools presented in the previous section fit into one or more
software ‘ecosystems’, by which we mean communities of software
developers linked by an overarching organisation, technology or
language. Software is not developed in isolation but in a social context
(Dhir and Dhir 2017), three of these ecosystems from which several open
source tools for geographic analysis in transport planning have — R,
Python and QGIS — are described below.

Other open source ecosystems include those surrounding the languages
JavaScript, Julia and Rust, and the GUI-based Java traffic management
system [IRIS](http://iris.dot.state.mn.us/). R, Python and QGIS
ecosystems were selected due to their maturity, wide uptake in industry
and academia and, above all, for their mature support for geographic
analysis.
<!-- They have also seen impressive growth in popularity over the past decade, suggesting they are future proof. -->

## R

R is a “a language and environment for statistical computing and
graphics” (R Core Team 2019). First announced and released as a binary
program in 1993 by University of Aukland statisticians Robert Gentleman
and Ross Ihaka, the project was only open sourced and released under the
conditions of the GNU General Public License (GPL) in 1995, thanks to
input from one of R’s first international collaborators, Martin Mächler
of ETH Zurich (Ihaka 1998). This history highlight’s how open source
software development is an inherently collaborative process, usually
involving people from many different countries and backgrounds.

R has several strengths from the perspective of transport planning and
has an active community of developers working between academia and
industry. Strengths include support for with temporal and geographic
data, outstanding visualisation capabilities, and support for a very
wide range of statistical techniques, many of which are useful in
transport problems (Lovelace and Ellison 2018b). R is a statistical
statistical programming language, meaning the base R installation can
solve a wide range of problems, including generalised linear models
(GLMs, implemented with the function `glm`) and constrained optimisation
problems that appear frequently in transport research. Additional
capabilities are supported by 10,000+ packages that can be installed
from a central repository with commands such as
`install.packages("stplanr")`.\[11\]

A good example of a transport problem that R’s statistical capabilities
are well suited to solving is mode choice. Unimodal models estimating
mode share (or the logit thereof) can use R’s inbuilt statistical
capabilities, as demonstrated in the Propensity to Cycle Tool project
(Lovelace et al. 2017). More sophisticated multinomial models are needed
when estimating mode share across multiple travel options such as walk,
cycle, bus (Mart’ın and P’aez 2019). R has mature support for such
models via the `multinom` function in the long-standing package `nnet`
(Venables and Ripley 2002), as demonstrated by [Germán
Rodríguez](https://data.princeton.edu/wws509/r/c6s2). Subsequent
packages provide additional methods for estimating mode split (Hasan,
Wang, and Mahani 2016; Croissant 2019). Appollo and mlr3 are recently
developed examples of R packages providing support for sophisticated
choice models and cutting edge machine learning functionality,
respectively.

<!-- [@hess_apollo_2019;@bischl_mlr_2016]. -->

R is well known for having outstanding statistical analysis and
modelling capabilities, of the type useful in transport planning. Less
known is that R also has a mature ecosystem for working with geographic
data, making it well suited to the task of integrating geographic
analysis in transport planning: R excels at doing modelling *and*
geographic analysis. This is particular interest here because, as
outlined in previous sections, ‘context switching’ between programs for
statistical and geographic analysis is time consuming.\[12\] Support for
geographic data and methods have a long history in R (Bivand 2006;
Pebesma et al. 2015; Bivand, Pebesma, and G’omez-Rubio 2013). The
development of R’s spatial capabilities are well documented elsewhere
\[link to other articles in the special edition\]. However, a few
advances are worth mentioning due to their relevance to transport
transport planning. The package `sf` (Pebesma 2018) provides a unified
and high performance system for working geographic lines (in addition to
its support for points and polygons), which can be used to represent
roads. Building on `sf`, the package `stplanr` (Lovelace and Ellison
2018b) provides many functions for working with geographic transport
data, including `overline` which enables thousands routes to be
aggregated to create route networks (Morgan and Lovelace, in press) and
`dl_stats19`, which has evolved into the `stats19` package (Lovelace et
al. 2019). Geographic data visualisation, cartography, is another area
where R excels, with packages such as `tmap` (Tennekes 2018) providing
powerful functions for map making. These and many other packages for
working with geographic data in R are described in detail in
*Geocomputation with R* (Lovelace, Nowosad, and Meunchow 2019). Chapter
12 this of this open source book is dedicated to transport applications,
and provides a good starting point for learning more about using R’s
impressive geographic capabilities for transport planning.

## Python

Python is a general-purpose programming language originally conceived in
the late 1980s and first released in 1991 (Rossum 1995). The language
was designed from a computer science perspective, with a focus on code
elegance and consistency, rather than R’s focus on statistical
functionality. However, Python has become very popular for data analysis
and ‘data science’ thanks to packages such as
[Pandas](https://github.com/pandas-dev/pandas), and SciKitLearn
(McKinney 2017). Due to its range of features, large open source
community, and flexibility, Python has been used as a ‘glue’ language to
interact with many other software systems. It is a highly diverse
language that is widely used in domains ranging from web development
(Grinberg 2018), to computer vision and (Zafar et al. 2018) text
analysis (Bengfort, Bilbro, and Ojeda 2018).

Of particular interest here is Python’s support for geographic data.
There are dozens of geographic projects written in Python, ranging from
the use of the language to teach low level geographic concepts and
algorithms (Xiao 2016) to its use as an interface to libraries such as
GDAL. Dozens of Python packages have been published for solving specific
geographic problems, ranging from the processing of scientific
gravimetric measurements (McCubbine et al. 2018) to handling remote
sensing data for Ireland (Serbin and Green 2018), both of which could
have transport applications. Furthermore, Python is used as the language
of choice of choice for command-line interfaces to the popular
proprietary GIS ArcMAP (Zandbergen 2015).

More general purpose package for handling spatial datasets that could be
used for transport research include [GeoPandas](http://geopandas.org/),
for handling vector data such as roads and
[rasterio](https://rasterio.readthedocs.io/en/stable/) for handling
raster datasets. Building on such foundations, a number of Python
developers have written packages with a transport focus. This include
OSMnx (Boeing 2017), for downloading and analysing street network data
from OpenStreetMap and the recent and ambitious project (Pappalardo et
al. 2019b) which, despite limited documentation at the time of writing,
sets out to create a framework for modelling transport systems.

Because Python is a general purpose language, it has been used as the
basis of transport applications that go beyond the transport planning
remit of this paper. A couple of projects are worth mentioning to give
an indication of the wider Python transport ecosystem.
[Itinerum](https://github.com/TRIP-Lab) is an open source travel survey
development project, which includes a backend written in Python and
smartphone apps (Patterson et al. 2019). A similar project is
[E-mission](https://github.com/e-mission) (Shankari et al. 2018) the
backend of which is partly written in Python.

## QGIS

QGIS is a cross-platform desktop GIS application with a huge user base
(likely the most popular GIS software in the world) and more than 1000
community supported plugins (QGIS Development Team 2019). QGIS itself is
written primarily in C++ and Python, meaning that there is strong
symbiosis between the Python and QGIS ecosystems. In fact the majority
of QGIS plugins are written in Python, meaning that Python developers
can use QGIS as a platform for providing users with a graphical user
interface and, conversely, QGIS users can learn to use a CLI, via QGIS’s
Python console.

A good example of the flexibility of QGIS’s plugin model, and
illustrating the wider point that open source software tends to be
modular and do ‘one thing well’, is that sDNA, mentioned in Section
<a href="#the-current-landscape">3</a> can be used in QGIS via the sDNA
plugin (Chan and Cooper 2019). Indeed, the open source transport
modelling framework MATSim also benefits from being used alongside QGIS,
for road network editing and visualisation (Horni, Nagel, and Axhausen
2016b). QGIS plugins and extensions specifically designed for transport
planning applications include the AwaP-IC walkability analysis plugin
(Majic and Pafka 2019), extensions to QGIS’s Processing model
development framework for assessing road network completeness (Sehra,
Singh, and Rai 2017) and the ORS (OpenRouteService) plugin, for
multi-modal routing.

QGIS can also be used as a self-standing application for transport data
analysis. Ilayaraja (2013), for example, used QGIS as the platform of
choice for analysing street networks using the [Road Graph
plugin](https://docs.qgis.org/2.14/en/docs/user_manual/plugins/plugins_road_graph.html),
which ships with QGIS by default. Dong et al. (2016), to provide another
example, used QGIS as the basis of geographic analysis of route network
efficiency. Hundreds of other transport planning projects have used QGIS
for the mapping and geographic analysis component of the work and, due
to the application’s user friendly GUI, it is rapidly gaining in
popularity among government transport planning departments, including
Transport for Wales and Transport for Greater Manchester.

# Conclusion

Geographic analysis is an important yet often under-appreciated aspect
of transport planning, and looks set to play a more prominent role in
transport policy-making due to technological, data and policy drivers of
change. In the context of now policy drivers — including the obesity
crisis, air pollution concerns and the ‘climate emergency’ that has been
declared by some city authorities — many transport planners have been
tasked with new sustainable transport targets. These include
discouraging energy intensive modes, particularly car use, and enabling
more walking and cycling (Hickman, Ashiru, and Banister 2011) .
Furthermore, in the age of evidence-based policy, open data and citizen
science, there is an onus on practitioners to provide solutions that are
transparent, accessible and, increasingly, participatory (Banister 2008;
Peters 2020).

This poses a challenge to incumbent transport planning software which is
expensive and thereby inaccessible to most people, monolithic and (to a
greater or lesser extent) limited in terms of geographic capabilities,
particularly in relation to publicly accessible interactive
visualisation and adaptability. The new planning priorities also present
opportunities, in terms of institutional processes (Beddoe et al. 2009),
but also new technologies that are explicitly designed to enable more
participatory, transparent and community-driven transport planning
processes. A shift to open source planning tools in general, and open
source tools for local planning in particular, can help help tackle
wider problems, including the ‘crisis of participatory planning’ (Legacy
2016), feelings of dis-empowerment due to lack of opportunities to
engage in democratic processes — which some have blamed for the election
of populist leaders and the UK Brexit vote (Monbiot 2017) — and low
levels of data and software literacy (Christozov and Rasheva-Yordanova
2017). A key feature of geographically localised transport plans is that
they encourage participation by local residents, who have access to
information about their local area that goes beyond the datasets beyond
the reach of remote planners. And a key feature of open software is that
anyone can use it, encouraging citizen engagement.

Partly in response to these pressures and challenges, a number of open
source transport planning tools have emerged, notably MATSim, SUMO and
sDNA, as outlined in Section 4. Following the Unix philosophy of
modularity (Gancarz 2003), each of these tools has a particular niche.
However, despite a long history of geographic thinking in transport
planning and calls to strengthen the links between GIS and transport
software (Loidl et al. 2016) but none of the open source solutions
reviewed provide ‘in house’ GIS capabilities of the type needed for an
integrated transport planning workflow in which a single piece of
software can be used to import a range data, undertake statistical
analysis and modelling and plot the results in interactive maps,
e.g. for the design and modelling of new walking and cycling networks.

With a view to the future of transport planning software, three
established ‘software ecosystems’, each of which has a substantial
following and large community of developers building extensions, were
reviewed with respect to their capacity to support geographic analysis
in transport planning. The literature shows that R, Python and QGIS
communities have already developed several tools for transport planning
that, when combined with other open source solutions, can solve a very
wide range of spatial transport planning problems. Although each
ecosystem is mature (yet still growing), their use in transport planning
is still in a nascent phase, suggesting that much innovation, evolution
and consolidation will occur before any strong conclusions about which
is most appropriate for different transport planning tasks can be made.
However, tentative guidance can be made, based on the origins and
direction of each project: for statistically-orientated projects in
which interactive online visualisation is vital, R provides a strong
foundation; for applications in which general purpose languages and
interoperability with other frameworks, and integration with other
software frameworks, Python may be the most appropriate option; and when
a user friendly interface and rapid map making without need for
programming skills are required, QGIS may be suitable. There is a huge
amount of overlap between the three ecosystems and, in practice, the
prior experience and preferences of transport planners may be more
important than functionality.

As the FOSS philosophy described in Section
<a href="#new-tools-of-the-trade"><strong>??</strong></a> emphasises,
open source software by its very nature is collaborative, innovative and
evolving (Gancarz 2003), allowing it to out-compete and eventually
dominate in sectors from machine learning to web development. The review
of capabilities in open source software communities clearly shows that
high-performance and innovative solutions are already available in the
‘ecological niche’ of geographic analysis for transport planning.
Given the nascent nature of many of the transport-oriented packages,
plugins and extensions in each ecosystem, fruitful directions of
research would explore the relative merits of different options, and
combinations of options, in terms of computer and programmer efficiency.
Furthermore, the modular and ‘pluginable’ nature of open source software
suggests there are great opportunities for integration: could there be R
and Python interfaces to MATSim, SUMO and sDNA? And from a research
perspective, how can the growth of open source solutions for geographic
transport data analysis be monitored to identify ‘tipping points’ in
practitioners’ uptake of open source solutions?

These considerations wider questions, about if and when will open source
software rise to ascendancy in the wider field of transport planning.
Returning to the most urgent policy driver of climate change mitigation,
it is clear than a step change is needed in transport interventions. If
these interventions are made on the basis of analysis undertaken in open
source software — enabling rigorous, transparent and reproducible
evidence that can easily be repeated in new settings and when new
datasets become available — they are all the more likely to succeed. In
this sense it may not be an exaggeration to say that open source
software can save the world.

# References

<div id="refs" class="references hanging-indent">

<div id="ref-anderson_applying_1991">

Anderson, Larry D. 1991. “Applying Geographic Information Systems to
Transportation Planning.” *Transportation Research Record*, no. 1305.

</div>

<div id="ref-aryandoust_cityscale_2019">

Aryandoust, Arsam, Oscar van Vliet, and Anthony Patt. 2019. “City-Scale
Car Traffic and Parking Density Maps from Uber Movement Travel Time
Data.” *Scientific Data* 6 (1): 1–18.
<https://doi.org/10.1038/s41597-019-0159-6>.

</div>

<div id="ref-banister_sustainable_2008">

Banister, David. 2008. “The Sustainable Mobility Paradigm.” *Transport
Policy* 15 (2): 73–80.
[https://doi.org/DOI: 10.1016/j.tranpol.2007.10.005](https://doi.org/DOI:%2010.1016/j.tranpol.2007.10.005).

</div>

<div id="ref-barthelemy_spatial_2011">

Barth’elemy, Marc. 2011. “Spatial Networks.” *Physics Reports* 499
(1–3): 1–101.

</div>

<div id="ref-batty_planning_1995">

Batty, Michael. 1995. “Planning Support Systems and the New Logic of
Computation.” *Regional Development Dialogue* 16 (1): 1–17.

</div>

<div id="ref-beddoe_overcoming_2009">

Beddoe, Rachael, Robert Costanza, Joshua Farley, Eric Garza, Jennifer
Kent, Ida Kubiszewski, Luz Martinez, et al. 2009. “Overcoming Systemic
Roadblocks to Sustainability: The Evolutionary Redesign of Worldviews,
Institutions, and Technologies.” *Proceedings of the National Academy of
Sciences* 106 (8): 2483–9. <https://doi.org/10.1073/pnas.0812570106>.

</div>

<div id="ref-bengfort_applied_2018">

Bengfort, Benjamin, Rebecca Bilbro, and Tony Ojeda. 2018. *Applied Text
Analysis with Python: Enabling Language-Aware Data Products with Machine
Learning*. " O’Reilly Media, Inc.".

</div>

<div id="ref-bivand_implementing_2006">

Bivand, Roger. 2006. “Implementing Spatial Data Analysis Software Tools
in R.” *Geographical Analysis* 38 (1): 23–40.
<https://doi.org/10.1111/j.0016-7363.2005.00672.x>.

</div>

<div id="ref-bivand_applied_2013">

Bivand, Roger, Edzer J Pebesma, and Virgilio G’omez-Rubio. 2013.
*Applied Spatial Data Analysis with R*. Vol. 747248717. Springer.

</div>

<div id="ref-blanchard_urbanaccess_2017">

Blanchard, Samuel D., and Paul Waddell. 2017. “Urbanaccess: Generalized
Methodology for Measuring Regional Accessibility with an Integrated
Pedestrian and Transit Network.” *Transportation Research Record* 2653
(1): 35–44.

</div>

<div id="ref-boeing_osmnx_2017">

Boeing, Geoff. 2017. “OSMnx: New Methods for Acquiring, Constructing,
Analyzing, and Visualizing Complex Street Networks.” *Computers,
Environment and Urban Systems* 65 (September): 126–39.
<https://doi.org/10.1016/j.compenvurbsys.2017.05.004>.

</div>

<div id="ref-boyce_forecasting_2015">

Boyce, David E., and Huw C. W. L. Williams. 2015. *Forecasting Urban
Travel: Past, Present and Future*. Edward Elgar Publishing.

</div>

<div id="ref-chan_using_2019">

Chan, Eric Yin Cheung, and Crispin HV Cooper. 2019. “Using Road Class as
a Replacement for Predicted Motorized Traffic Flow in Spatial Network
Models of Cycling.” *Scientific Reports* 9 (1): 1–12.

</div>

<div id="ref-christozov_data_2017">

Christozov, Dimitar, and Katia Rasheva-Yordanova. 2017. “Data Literacy.”
*International Journal of Digital Literacy and Digital Competence* 8
(2): 14–38. <https://doi.org/10.4018/ijdldc.2017040102>.

</div>

<div id="ref-coelho_this_2020">

Coelho, Jailton, Marco Tulio Valente, Luciano Milen, and Luciana L.
Silva. 2020. “Is This GitHub Project Maintained? Measuring the Level of
Maintenance Activity of Open-Source Projects.” *Information and Software
Technology* 122 (June): 106274.
<https://doi.org/10.1016/j.infsof.2020.106274>.

</div>

<div id="ref-croissant_mlogit_2019">

Croissant, Yves. 2019. *Mlogit: Multinomial Logit Models*.

</div>

<div id="ref-dhir_adoption_2017">

Dhir, Swati, and Sanjay Dhir. 2017. “Adoption of Open-Source Software
Versus Proprietary Software: An Exploratory Study.” *Strategic Change*
26 (4): 363–71. <https://doi.org/10.1002/jsc.2137>.

</div>

<div id="ref-ortuzars._modelling_2011">

Dios Ort’uzar S., Juan de, and Luis G. Willumsen. 2011. *Modelling
Transport*. Fourth edition. Chichester, West Sussex, United Kingdom:
John Wiley & Sons.

</div>

<div id="ref-dong_population-weighted_2016">

Dong, Lei, Ruiqi Li, Jiang Zhang, and Zengru Di. 2016.
“Population-Weighted Efficiency in Transportation Networks.”
*Scientific Reports* 6 (May): 26377.
<https://doi.org/10.1038/srep26377>.

</div>

<div id="ref-ebdon_spans_1992">

Ebdon, David. 1992. “SPANSA Quadtree-Based GIS.” *Computers &
Geosciences*, GIS Design Models, 18 (4): 471–75.
<https://doi.org/10.1016/0098-3004(92)90077-5>.

</div>

<div id="ref-fleischmann_momepy_2019">

Fleischmann, Martin. 2019. “MOMEPY: Urban Morphology Measuring Toolkit.”
*Journal of Open Source Software* 4 (43): 1807.

</div>

<div id="ref-franco-bedoya_open_2017">

Franco-Bedoya, Oscar, David Ameller, Dolors Costal, and Xavier Franch.
2017. “Open Source Software Ecosystems: A Systematic Mapping.”
*Information and Software Technology* 91: 160–85.

</div>

<div id="ref-gancarz_linux_2003">

Gancarz, Mike. 2003. *Linux and the Unix Philosophy*. Digital Press.

</div>

<div id="ref-goodman_scenarios_2019">

Goodman, Anna, Ilan Fridman Rojas, James Woodcock, Rachel Aldred,
Nikolai Berkoff, Malcolm Morgan, Ali Abbas, and Robin Lovelace. 2019.
“Scenarios of Cycling to School in England, and Associated Health and
Carbon Impacts: Application of the ‘Propensity to Cycle Tool’.” *Journal
of Transport & Health* 12 (March): 263–78.
<https://doi.org/10.1016/j.jth.2019.01.008>.

</div>

<div id="ref-grabowicz_social_2012">

Grabowicz, Przemyslaw A., Jos’e J. Ramasco, Esteban Moro, Josep M.
Pujol, and Victor M. Eguiluz. 2012. “Social Features of Online Networks:
The Strength of Intermediary Ties in Online Social Media.” *PloS One* 7
(1): e29358.

</div>

<div id="ref-graser_movingpandas_2019">

Graser, Anita. 2019. “Movingpandas: Efficient Structures for Movement
Data in Python.” *GIForum* 1: 54–68.

</div>

<div id="ref-grinberg_flask_2018">

Grinberg, Miguel. 2018. *Flask Web Development: Developing Web
Applications with Python*. " O’Reilly Media, Inc.".

</div>

<div id="ref-hackl_promoting_2019">

Hackl, Roland, Clemens Raffler, Michael Friesenecker, Hans Kramar,
Robert Kalasek, Aggelos Soteropoulos, Susanne Wolf-Eberl, Patrick Posch,
and Rupert Tomschy. 2019. “Promoting Active Mobility: Evidence-Based
Decision-Making Using Statistical Models.” *Journal of Transport
Geography* 80 (October): 102541.
<https://doi.org/10.1016/j.jtrangeo.2019.102541>.

</div>

<div id="ref-hadfield_financing_2019">

Hadfield, Paris, and Nicole Cook. 2019. “Financing the Low-Carbon City:
Can Local Government Leverage Public Finance to Facilitate Equitable
Decarbonisation?” *Urban Policy and Research* 37 (1): 13–29.
<https://doi.org/10.1080/08111146.2017.1421532>.

</div>

<div id="ref-harrison_environmental_2017">

Harrison, R. M., and R. E. Hester. 2017. *Environmental Impacts of Road
Vehicles: Past, Present and Future*. Royal Society of Chemistry.

</div>

<div id="ref-hasan_fast_2016">

Hasan, Asad, Zhiyu Wang, and Alireza S. Mahani. 2016. “Fast Estimation
of Multinomial Logit Models: R Package Mnlogit.” *Journal of Statistical
Software* 75 (1): 1–24. <https://doi.org/10.18637/jss.v075.i03>.

</div>

<div id="ref-hickman_transitions_2011">

Hickman, Robin, Olu Ashiru, and David Banister. 2011. “Transitions to
Low Carbon Transport Futures: Strategic Conversations from London and
Delhi.” *Journal of Transport Geography*, Special section on Alternative
Travel futures, 19 (6): 1553–62.
<https://doi.org/10.1016/j.jtrangeo.2011.03.013>.

</div>

<div id="ref-hildebrand_comparative_2014">

Hildebrand, Cisilia, and Stina Hörtin. 2014. *A Comparative Study
Between Emme and Visum with Respect to Public Transport Assignment*.

</div>

<div id="ref-hollander_transport_2016">

Hollander, Yaron. 2016. *Transport Modelling for a Complete Beginner*.
CTthink\!

</div>

<div id="ref-horni_multi-agent_2016">

Horni, Andreas, Kai Nagel, and Kay W. Axhausen. 2016a. *The Multi-Agent
Transport Simulation MATSim*. Ubiquity Press.
<https://www.ubiquitypress.com/site/books/10.5334/baw/>.

</div>

<div id="ref-horni_multiagent_2016">

———. 2016b. *The Multi-Agent Transport Simulation MATSim*. Ubiquity
Press. <https://doi.org/10.5334/baw>.

</div>

<div id="ref-hull_policy_2008">

Hull, Angela. 2008. “Policy Integration: What Will It Take to Achieve
More Sustainable Transport Solutions in Cities?” *Transport Policy*, New
Developments in Urban Transportation Planning, 15 (2): 94–103.
<https://doi.org/10.1016/j.tranpol.2007.10.004>.

</div>

<div id="ref-iacono_measuring_2010">

Iacono, Michael, Kevin J. Krizek, and Ahmed El-Geneidy. 2010. “Measuring
Non-Motorized Accessibility: Issues, Alternatives, and Execution.”
*Journal of Transport Geography* 18 (1): 133–40.
<https://doi.org/10.1016/j.jtrangeo.2009.02.002>.

</div>

<div id="ref-ihaka_future_1998">

Ihaka, Ross. 1998. “R: Past and Future History.” *Computing Science and
Statistics* 392396.

</div>

<div id="ref-ilayaraja_road_2013">

Ilayaraja, K. 2013. “Road Network Analysis in Neyveli Township,
Cuddalore District by Using Quantum GIS.” *Indian Journal of Computer
Science and Engineering* 4 (1).

</div>

<div id="ref-jappinen_modelling_2013">

Jäppinen, Sakari, Tuuli Toivonen, and Maria Salonen. 2013. “Modelling
the Potential Effect of Shared Bicycles on Public Transport Travel Times
in Greater Helsinki: An Open Data Approach.” *Applied Geography* 43:
13–24.

</div>

<div id="ref-kampa_human_2008">

Kampa, Marilena, and Elias Castanas. 2008. “Human Health Effects of Air
Pollution.” *Environmental Pollution*, Proceedings of the 4th
International Workshop on Biomonitoring of Atmospheric Pollution (With
Emphasis on Trace Elements), 151 (2): 362–67.
<https://doi.org/10.1016/j.envpol.2007.06.012>.

</div>

<div id="ref-kilian_emerging_2018">

Kilian, Jason, and Masashi Kitazawa. 2018. “The Emerging Risk of
Exposure to Air Pollution on Cognitive Decline and Alzheimer’s
Disease–Evidence from Epidemiological and Animal Studies.” *Biomedical
Journal*.

</div>

<div id="ref-klosterman_what_1999">

Klosterman, R. E. 1999. “The What If? Collaborative Planning Support
System.” *Environment and Planning B: Planning and Design* 26 (3):
393–408. <https://doi.org/10.1068/b260393>.

</div>

<div id="ref-knuth_art_1997">

Knuth, Donald E. 1997. *The Art of Computer Programming: Volume 1:
Fundamental Algorithms*. Addison-Wesley Professional.

</div>

<div id="ref-kotusevski_review_2009">

Kotusevski, G., and K. A. Hawick. 2009. “A Review of Traffic Simulation
Software.” *Research Letters in the Information and Mathematical
Sciences* 13: 35–54. <https://mro.massey.ac.nz/handle/10179/4506>.

</div>

<div id="ref-larsen_build_2013">

Larsen, Jacob, Zachary Patterson, and Ahmed El-Geneidy. 2013. “Build It.
But Where? The Use of Geographic Information Systems in Identifying
Locations for New Cycling Infrastructure.” *International Journal of
Sustainable Transportation* 7 (4): 299–317.

</div>

<div id="ref-legacy_there_2016">

Legacy, Crystal. 2016. “Is There a Crisis of Participatory Planning?”
*Planning Theory* 16 (4): 425–42.
<https://doi.org/10.1177/1473095216667433>.

</div>

<div id="ref-levinson_network_2012">

Levinson, David. 2012. “Network Structure and City Size.” *PloS One* 7
(1): e29721. <https://doi.org/10.1371/journal.pone.0029721>.

</div>

<div id="ref-liao_largescale_2018">

Liao, Siyu, Liutong Zhou, Xuan Di, Bo Yuan, and Jinjun Xiong. 2018.
“Large-Scale Short-Term Urban Taxi Demand Forecasting Using Deep
Learning.” In *2018 23rd Asia and South Pacific Design Automation
Conference (ASP-DAC)*, 428–33. IEEE.

</div>

<div id="ref-lindsey_minnesota_2013">

Lindsey, Greg, Steve Hankey, Xize Wang, and Junzhou Chen. 2013. “The
Minnesota Bicycle and Pedestrian Counting Initiative: Methodologies for
Non-Motorized Traffic Monitoring.” Minnesota Department of
Transportation.

</div>

<div id="ref-loidl_gis_2016">

Loidl, Martin, Gudrun Wallentin, Rita Cyganski, Anita Graser, Johannes
Scholz, and Eva Haslauer. 2016. “GIS and Transport
Modeling—Strengthening the Spatial Perspective.” *ISPRS International
Journal of Geo-Information* 5 (6): 84.
<https://doi.org/10.3390/ijgi5060084>.

</div>

<div id="ref-lopez_microscopic_2018">

Lopez, Pablo Alvarez, Michael Behrisch, Laura Bieker-Walz, Jakob
Erdmann, Yun-Pang Flötteröd, Robert Hilbrich, Leonhard Lücken, Johannes
Rummel, Peter Wagner, and Evamarie WieBner. 2018. “Microscopic Traffic
Simulation Using Sumo.” In *2018 21st International Conference on
Intelligent Transportation Systems (ITSC)*, 2575–82. IEEE.

</div>

<div id="ref-lovelace_big_2016">

Lovelace, Robin, Mark Birkin, Philip Cross, and Martin Clarke. 2016.
“From Big Noise to Big Data: Toward the Verification of Large Data
Sets for Understanding Regional Retail Flows.” *Geographical Analysis*
48 (1): 59–81. <https://doi.org/10.1111/gean.12081>.

</div>

<div id="ref-lovelace_stplanr:_2018">

Lovelace, Robin, and Richard Ellison. 2018a. “Stplanr: A Package for
Transport Planning.” *The R Journal* 10 (2): 7–23.
<https://doi.org/10.32614/RJ-2018-053>.

</div>

<div id="ref-lovelace_stplanr_2018">

———. 2018b. “Stplanr: A Package for Transport Planning.” *The R Journal*
10 (2): 7–23. <https://doi.org/10.32614/RJ-2018-053>.

</div>

<div id="ref-lovelace_propensity_2017">

Lovelace, Robin, Anna Goodman, Rachel Aldred, Nikolai Berkoff, Ali
Abbas, and James Woodcock. 2017. “The Propensity to Cycle Tool: An Open
Source Online System for Sustainable Transport Planning.” *Journal of
Transport and Land Use* 10 (1). <https://doi.org/10.5198/jtlu.2016.862>.

</div>

<div id="ref-lovelace_stats19_2019">

Lovelace, Robin, Malcolm Morgan, Layik Hama, Mark Padgham, and M
Padgham. 2019. “Stats19 A Package for Working with Open Road Crash
Data.” *Journal of Open Source Software* 4 (33): 1181.
<https://doi.org/10.21105/joss.01181>.

</div>

<div id="ref-lovelace_geocomputation_2019">

Lovelace, Robin, Jakub Nowosad, and Jannes Meunchow. 2019.
*Geocomputation with R*. CRC Press. <http://robinlovelace.net/geocompr>.

</div>

<div id="ref-lofgren_considering_2018">

Löfgren, Sofia, Kristina L. Nilsson, and Charlotta M. Johansson. 2018.
“Considering Landscape in Strategic Transport Planning.”
*Transportation Research Part D: Transport and Environment* 65
(December): 396–408. <https://doi.org/10.1016/j.trd.2018.09.001>.

</div>

<div id="ref-majic_awap-icopen-source_2019">

Majic, Ivan, and Elek Pafka. 2019. “AwaP-IC—an Open-Source GIS Tool for
Measuring Walkable Access.” *Urban Science* 3 (2): 48.

</div>

<div id="ref-martin_individual_2019">

Mart’ın, Bel’en, and Antonio P’aez. 2019. “Individual and Geographic
Variations in the Propensity to Travel by Active Modes in
Vitoria-Gasteiz, Spain.” *Journal of Transport Geography* 76: 103–13.

</div>

<div id="ref-mccubbine_gsolve_2018">

McCubbine, Jack, Fabio Caratori Tontini, Vaughan Stagpoole, Euan Smith,
and Grant O’NABrie. 2018. “Gsolve, a Python Computer Program with a
Graphical User Interface to Transform Relative Gravity Survey
Measurements to Absolute Gravity Values and Gravity Anomalies.”
*SoftwareX* 7: 129–37.

</div>

<div id="ref-mckinney_python_2017">

McKinney, Wes. 2017. *Python for Data Analysis: Data Wrangling with
Pandas, NumPy, and IPython*. 2 edition. Sebastopol, California: O’Reilly
Media.

</div>

<div id="ref-miller_potential_1999">

Miller, Harvey J. 1999. “Potential Contributions of Spatial Analysis to
Geographic Information Systems for Transportation (GIS-T).”
*Geographical Analysis* 31 (4): 373–99.
<https://doi.org/10.1111/j.1538-4632.1999.tb00991.x>.

</div>

<div id="ref-moeckel_trends_2018">

Moeckel, Rolf, Carlos Llorca Garcia, Ana Tsui Moreno Chou, and Matthew
Bediako Okrah. 2018. “Trends in Integrated Land Use/Transport Modeling:
An Evaluation of the State of the Art.” *Journal of Transport and Land
Use* 11 (1). <https://doi.org/10.5198/jtlu.2018.1205>.

</div>

<div id="ref-monbiot_out_2017">

Monbiot, George. 2017. *Out of the Wreckage: A New Politics for an Age
of Crisis*. Brooklyn, NY: Verso Books.

</div>

<div id="ref-morgan_opentripplanner_2019">

Morgan, Malcolm, Marcus Young, Robin Lovelace, and Layik Hama. 2019.
“OpenTripPlanner for R.” *Journal of Open Source Software* 4 (44):
1926. <https://doi.org/10.21105/joss.01926>.

</div>

<div id="ref-moriarty_prospects_2008">

Moriarty, Patrick, and Damon Honnery. 2008. “The Prospects for Global
Green Car Mobility.” *Journal of Cleaner Production* 16 (16): 1717–26.
<https://doi.org/10.1016/j.jclepro.2007.10.025>.

</div>

<div id="ref-morrison_energy_2018">

Morrison, Robbie. 2018. “Energy System Modeling: Public Transparency,
Scientific Reproducibility, and Open Development.” *Energy Strategy
Reviews* 20: 49–63.

</div>

<div id="ref-neteler_open_2008">

Neteler, Markus, and Helena Mitasova. 2008. *Open Source GIS: A GRASS
GIS Approach*. Third. New York, NY: Springer.

</div>

<div id="ref-oflaherty_transport_1997">

O’Flaherty, Coleman, and Michael GH Bell. 1997. *Transport Planning and
Traffic Engineering*. Elsevier.

</div>

<div id="ref-pappalardo_scikit-mobility:_2019">

Pappalardo, Luca, Gianni Barlacchi, Filippo Simini, and Roberto
Pellungrini. 2019a. “Scikit-Mobility: An Open-Source Python Library for
Human Mobility Analysis and Simulation.” *arXiv:1907.07062 \[Physics\]*,
July. <http://arxiv.org/abs/1907.07062>.

</div>

<div id="ref-pappalardo_scikitmobility_2019">

———. 2019b. “Scikit-Mobility: An Open-Source Python Library for Human
Mobility Analysis and Simulation.” *arXiv:1907.07062 \[Physics\]*, July.
<http://arxiv.org/abs/1907.07062>.

</div>

<div id="ref-parkin_designing_2018">

Parkin, John. 2018. *Designing for Cycle Traffic: International
Principles and Practice*. ICE Publishing.
<https://www.icevirtuallibrary.com/isbn/9780727763495>.

</div>

<div id="ref-patterson_itinerum_2019">

Patterson, Zachary, Kyle Fitzsimmons, Stewart Jackson, and Takeshi
Mukai. 2019. “Itinerum: The Open Smartphone Travel Survey Platform.”
*SoftwareX* 10 (July): 100230.
<https://doi.org/10.1016/j.softx.2019.04.002>.

</div>

<div id="ref-pebesma_simple_2018">

Pebesma, Edzer. 2018. “Simple Features for R: Standardized Support for
Spatial Vector Data.” *The R Journal*.
<https://journal.r-project.org/archive/2018/RJ-2018-009/index.html>.

</div>

<div id="ref-pebesma_software_2015">

Pebesma, Edzer, Roger Bivand, Paulo Justiniano Ribeiro, and others.
2015. “Software for Spatial Statistics.” *Journal of Statistical
Software* 63 (1): 1–8.
<http://brage.bibsys.no/xmlui/bitstream/id/320781/Pebesma_Bivand_Ribeiro.pdf>.

</div>

<div id="ref-pensa_supporting_2013">

Pensa, Stefano, Elena Masala, and Isabella M. Lami. 2013. “Supporting
Planning Processes by the Use of Dynamic Visualisation.” In *Planning
Support Systems for Sustainable Urban Development*, 451–67. Springer.

</div>

<div id="ref-peters_citizen_2020">

Peters, Michael A. 2020. “Citizen Science and Ecological Democracy in
the Global Science Regime: The Need for Openness and Participation.”
*Educational Philosophy and Theory* 52 (3): 221–26.
<https://doi.org/10.1080/00131857.2019.1584148>.

</div>

<div id="ref-pettit_australian_2014">

Pettit, C. J., J Barton, X Goldie, R Sinnott, R Stimson, and T Kvan.
2014. “The Australian Urban Intelligence Network Supporting Smart
Cities.” In *Smart Cities and Planning Support Systems*, edited by S
Geertma, J Stillwell, J Ferreira, and J Goodspeed. Springer.

</div>

<div id="ref-pucher_making_2008">

Pucher, John, and Ralph Buehler. 2008. “Making Cycling Irresistible:
Lessons from the Netherlands, Denmark and Germany.” *Transport Reviews*
28 (4): 495–528. <https://doi.org/10.1080/01441640701806612>.

</div>

<div id="ref-qgisdevelopmentteam_qgis_2019">

QGIS Development Team. 2019. “QGIS Geographic Information System.” Open
Source Geospatial Foundation.

</div>

<div id="ref-rcoreteam_language_2019">

R Core Team. 2019. “R: A Language and Environment for Statistical
Computing.” Vienna, Austria: R Foundation for Statistical Computing.

</div>

<div id="ref-rodrigue_geography_2013">

Rodrigue, Jean-Paul, Claude Comtois, and Brian Slack. 2013. *The
Geography of Transport Systems*. Third. London, New York: Routledge.

</div>

<div id="ref-rossum_python_1995">

Rossum, Guido. 1995. “Python Reference Manual.” Amsterdam, The
Netherlands, The Netherlands: CWI (Centre for Mathematics; Computer
Science).

</div>

<div id="ref-sallis_use_2016">

Sallis, James F., Fiona Bull, Ricky Burdett, Lawrence D. Frank, Peter
Griffiths, Billie Giles-Corti, and Mark Stevenson. 2016. “Use of Science
to Guide City Planning Policy and Practice: How to Achieve Healthy and
Sustainable Future Cities.” *The Lancet* 388 (10062): 2936–47.

</div>

<div id="ref-salter_digital_2009">

Salter, Jonathan D., Cam Campbell, Murray Journeay, and Stephen R. J.
Sheppard. 2009. “The Digital Workshop: Exploring the Use of Interactive
and Immersive Visualisation Tools in Participatory Planning.” *Journal
of Environmental Management*, Collaborative GIS for spatial decision
support and visualization, 90 (6): 2090–2101.
<https://doi.org/10.1016/j.jenvman.2007.08.023>.

</div>

<div id="ref-sehra_assessing_2017">

Sehra, Sukhjit, Jaiteg Singh, and Hardeep Rai. 2017. “Assessing
OpenStreetMap Data Using Intrinsic Quality Indicators: An Extension to
the QGIS Processing Toolbox.” *Future Internet* 9 (2): 15.

</div>

<div id="ref-serbin_opensourced_2018">

Serbin, Guy, and Stuart Green. 2018. “Open-Sourced Remote Sensing Data
Management with the Irish Earth Observation (IEO) Python Module.”
*Preprints.org*, May.
<https://doi.org/10.20944/preprints201805.0470.v1>.

</div>

<div id="ref-shankari_emission_2018">

Shankari, K., Mohamed Amine Bouzaghrane, Samuel M. Maurer, Paul Waddell,
David E. Culler, and Randy H. Katz. 2018. “E-Mission: An Open-Source,
Smartphone Platform for Collecting Human Travel Data.” *Transportation
Research Record* 2672 (42): 1–12.
<https://doi.org/10.1177/0361198118770167>.

</div>

<div id="ref-sherman_desktop_2008">

Sherman, Gary. 2008. *Desktop GIS: Mapping the Planet with Open Source
Tools*. Pragmatic Bookshelf.

</div>

<div id="ref-singleton_geographic_2019">

Singleton, Alex, and Daniel Arribas-Bel. 2019. “Geographic Data
Science.” *Geographical Analysis*.

</div>

<div id="ref-te_brommelstroet_developing_2008">

te Brömmelstroet, Marco, and Luca Bertolini. 2008. “Developing Land Use
and Transport PSS: Meaningful Information Through a Dialogue Between
Modelers and Planners.” *Transport Policy* 15 (4): 251–59.
<https://doi.org/10.1016/j.tranpol.2008.06.001>.

</div>

<div id="ref-tennekes_tmap_2018">

Tennekes, Martijn. 2018. “Tmap: Thematic Maps in R.” *Journal of
Statistical Software, Articles* 84 (6): 1–39.
<https://doi.org/10.18637/jss.v084.i06>.

</div>

<div id="ref-timms_imagineering_2014">

Timms, Paul, Miles Tight, and David Watling. 2014. “Imagineering
Mobility: Constructing Utopias for Future Urban Transport.” *Environment
and Planning A* 46 (1): 78–93. <https://doi.org/10.1068/a45669>.

</div>

<div id="ref-tornberg_making_2018">

Tornberg, Patrik, and John Odhage. 2018. “Making Transport Planning More
Collaborative? The Case of Strategic Choice of Measures in Swedish
Transport Planning.” *Transportation Research Part A: Policy and
Practice* 118 (December): 416–29.
<https://doi.org/10.1016/j.tra.2018.09.020>.

</div>

<div id="ref-transport_systems_catapult_transport_2015">

Transport Systems Catapult. 2015. “The Transport Data Revolution.”
Government. Transport Systems Catapult.
<https://ts.catapult.org.uk/wp-content/uploads/2016/04/The-Transport-Data-Revolution.pdf>.

</div>

<div id="ref-tribby_highresolution_2012">

Tribby, Calvin P., and Paul a. Zandbergen. 2012. “High-Resolution
Spatio-Temporal Modeling of Public Transit Accessibility.” *Applied
Geography* 34 (May): 345–55.
<https://doi.org/10.1016/j.apgeog.2011.12.008>.

</div>

<div id="ref-vandenbulcke_mapping_2009">

Vandenbulcke, Gr’egory, Isabelle Thomas, Bas de Geus, Bart Degraeuwe,
Rudi Torfs, Romain Meeusen, and Luc Int Panis. 2009. “Mapping Bicycle
Use and the Risk of Accidents for Commuters Who Cycle to Work in
Belgium.” *Transport Policy* 16 (2): 77–87.
<https://doi.org/10.1016/j.tranpol.2009.03.004>.

</div>

<div id="ref-venables_modern_2002">

Venables, W. N., and B. D. Ripley. 2002. *Modern Applied Statistics with
S*. Fourth. New York: Springer. <http://www.stats.ox.ac.uk/pub/MASS4>.

</div>

<div id="ref-world_health_organization_global_2018">

World Health Organization. 2018. *Global Status Report on Road Safety
2018*. S.l.
<https://www.who.int/violence_injury_prevention/road_safety_status/2018/en/>.

</div>

<div id="ref-xiao_gis_2016">

Xiao, Ningchuan. 2016. *GIS Algorithms: Theory and Applications for
Geographic Information Science & Technology*. London.
<https://doi.org/10.4135/9781473921498>.

</div>

<div id="ref-xie_evolving_2011">

Xie, Feng, and David Levinson. 2011. *Evolving Transportation Networks*.
Transportation Research, Economics and Policy. New York:
Springer-Verlag. <https://www.springer.com/gp/book/9781441998033>.

</div>

<div id="ref-zafar_hands-convolutional_2018">

Zafar, Iffat, Giounona Tzanidou, Richard Burton, Nimesh Patel, and
Leonardo Araujo. 2018. *Hands-on Convolutional Neural Networks with
TensorFlow: Solve Computer Vision Problems with Modeling in TensorFlow
and Python*. Packt Publishing Ltd.

</div>

<div id="ref-zandbergen_python_2015">

Zandbergen, Paul A. 2015. *Python Scripting for ArcGIS*. Esri press.

</div>

</div>

1.   Articles about successful transport planners illustrate the point.
    Ben Hamilton-Baillie (1955 - 2019), for example, was an influential
    transport planner and street designer whose obituary emphasised the
    “hundreds of thousands of people who are safer and happier as a
    result of his achievements” (Tim Stornor, quoted in
    [TransportExtra](https://www.transportxtra.com/publications/local-transport-today/news/60655/obituary-ben-hamilton-baillie/)).

2.   See <https://www.cyclescape.org/> for an example of such a
    peer-to-peer transport planning tool.

3.  Transport is a major electoral issue in London and the current
    Mayor, Sadiq Kahn, has made tackling air pollution a policy
    priority. See
    [tfl.gov.uk/corporate/about-tfl/the-mayors-transport-strategy](https://tfl.gov.uk/corporate/about-tfl/the-mayors-transport-strategy).

4.   The current Mayor of Paris, Anne Hidalgo, sees transport as a
    priority and has plans to make public transport free. See
    [paris.fr](https://www.paris.fr/rechercher/transport).

5.   Bogotá has an innovative and prominent transport policy, led by the
    two times mayor Enrique Peñalosa, who has led the roll-out of major
    bus and cycleway projects in the city. See
    [sitp.gov.co](https://www.sitp.gov.co/).

6.   There is of course a close relationship between transport planning
    software and models because theoretical models can inform the
    direction of software developments, as was the case with the
    development of spatial interaction models (Boyce and Williams 2015).
    Conversely, ‘upstream’ developments in computer languages affect the
    range of models that can be implemented, as can be seen with the
    current shift towards cloud-based and more visual and interactive
    transport models such as the open source
    [Streetmix](https://streetmix.net) and the Institute of Transport
    Engineers endorsed [StreetPlan](https://streetplan.net) tools for
    visualising 1D street layouts and cloud-based transport planning
    services such as [Remix](https://www.remix.com/).

7.   UTPS stands for the UMT (Urban Mass Transportation Administration,
    an agency of the DoT responsible for transport planning)
    Transportation Planning System (UTPS).

8.   Thanks to Crispin Cooper, author of sDNA, for raising this barrier.

9.   Some tools can be used through multiple interfaces but most have a
    dominant interface type.

10.  See <https://www.fsf.org/about/what-is-free-software> for a full
    definition and context.

11.  Like Python packages, R packages are analogous to Apps on
    smartphones and plugins in QGIS (described below), that provide new
    functionality. Many implement recently developed statistical and
    computational techniques (some of which are accompanied by papers
    describing new methods in academic journals such as the *Journal for
    Statistical Software*) or provide interfaces to software written in
    other languages, meaning that R can provide transport researchers
    with access to many cutting-edge methods via a single system.

12.  The author has first hand experience of the costs of
    context-switching: during my PhD I used R for the statistical and
    modelling analysis, and then switched to QGIS for geographic
    analysis and visualisation. While this approach worked well, the
    cognitive burden of having to learn and manage two substantial
    programs was substantial.
