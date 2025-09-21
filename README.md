<table width="100%">
<tr>
    <td width="33%" align="center">
        <img src="https://github.com/user-attachments/assets/de094470-094d-4f7c-90c5-de2208b136a4" style="width:100%; height:auto;" />
    </td>
    <td width="33%" align="center">
        <img src="https://julialang.org/assets/infra/logo.svg" style="width:100%; height:auto;" />
    </td>
    <td width="33%" align="center">
        <img src="https://juliahealth.org/assets/images/logo.png" style="width:100%; height:auto;" />
    </td>
</tr>
</table>


# Google Summer of Code 2025 (The Julia Language) — JuliaHealth: Final Work Report  

Hey everyone, My name is Indu. I'm a final-year undergrad, doing my B.Tech in CSE (AI & ML) from a tier-3 college in India. Coming from this background, I've always been eager to explore opportunities beyond my campus and push myself through things like open-source. That's why GSoC was always on my mind — I've been drawn to it for a long time, and I knew I wanted to contribute to something meaningful. One thing led to another, and fortunately I got the chance to be a GSoC mentee in a lovely organization and community.

## Background

My GSoC journey actually started back in Jan–Feb, when I first came across the Julia organization. I decided to explore JuliaHealth, and honestly it turned out to be one of the best decisions I've made. I also got to work with my mentor, Jacob Zelko — truly the best mentor I could have asked for. 

At that time, Jacob suggested I try working on Patient Level Prediction (PLP). I went ahead and did that project, which became my first real experience with JuliaHealth. After finishing it, we realized there were still some important gaps in the ecosystem that needed to be filled before things like PLP could really stand on solid ground.

That's how my GSoC project started "Supporting Patient Level Pipelines within JuliaHealth". Instead of directly building prediction pipelines, the focus shifted to filling those gaps and creating the missing foundations.  
So this summer I split my work into two parts:

- **Phase 1 — HealthBase.jl:** added HealthTable support for OMOP CDM and some core preprocessing utilities.  
- **Phase 2 — OMOPCDMFeasibility.jl:** built a new package for pre- and post-cohort feasibility analysis.

## Phase 1: HealthBase.jl

The first part of my project was all about [HealthBase.jl](https://github.com/JuliaHealth/HealthBase.jl). This package acts as a backbone for having common namespace for functions and interfaces in the JuliaHealth ecosystem, so my focus here was to extend it with schema-aware OMOP CDM tables and add preprocessing utilities.

The idea was to make it easier for researchers to work directly with OMOP data in Julia without having to constantly worry about schema mismatches or messy preprocessing steps. I introduced a new HealthTable setup that understands the OMOP CDM structure, making it much more reliable for downstream tasks. Along with that, I added basic preprocessing functions that prepare data for further analysis or modeling.

I also helped improve the official documentation so new users can get started more easily: [HealthBase.jl Documentation](https://juliahealth.github.io/HealthBase.jl/)

This work basically laid the groundwork for anything that comes next — including feasibility studies and eventually full PLP pipelines.

**Pull Requests for HealthBase.jl:**

| Feature | Description | PR / Link |
|---------|-------------|-----------|
| HealthTable setup | Schema-aware support for OMOP CDM tables | [#30: Initial HealthTable setup and support](https://github.com/JuliaHealth/HealthBase.jl/pull/30) |

**Detailed Blog Posts on the official JuliaHealth Blog:**  
- [Phase 1 Report](https://juliahub.org/blog/phase1)

## Phase 2: OMOPCDMFeasibility.jl

Once the foundation was in place, I moved on to building a completely new package: [OMOPCDMFeasibility.jl](https://github.com/JuliaHealth/OMOPCDMFeasibility.jl). This package is designed to handle cohort feasibility analysis — both before and after cohort creation. Pre-cohort feasibility helps check if a study design or query is even practical before you run it, while post-cohort feasibility validates whether the cohorts you've built make sense and are usable.

To make this concrete, I implemented features for both pre- and post-cohort feasibility checks, along with clear documentation so the community can easily use and extend the package.

**Pull Requests for OMOPCDMFeasibility.jl:**

| Feature | Description | PR / Link |
|---------|-------------|-----------|
| Pre-Cohort Feasibility | Check feasibility before cohort creation | [#2: PreCohort Feasibility](https://github.com/JuliaHealth/OMOPCDMFeasibility.jl/pull/2) |
| Post-Cohort Feasibility | Validate cohorts after creation | [#3: Post Cohort Feasibility](https://github.com/JuliaHealth/OMOPCDMFeasibility.jl/pull/3) |
| Documentation | Clear user guide for the package | [#7: Documentation](https://github.com/JuliaHealth/OMOPCDMFeasibility.jl/pull/7) |

**Detailed Blog Posts on the official JuliaHealth Blog:**  
- [Phase 2 Report](https://juliahub.org/blog/phase2)

## Future Work

There's still plenty left to do. Some things I'd love to see built on top of this work are:

- Better preprocessing utilities — things like imputation, cohort filtering, and other data cleaning steps.  
- More built-in stats and visualization tools to make feasibility results easier to understand.  
- Getting all of this closer to PLP pipelines, so future contributors can plug models in more directly.

## Acknowledgements

Huge thanks to my mentor, Jacob S. Zelko (TheCedarPrince), for guiding me throughout the summer and always encouraging me to push further. And also to the JuliaHealth community — the support, discussions, and collaboration made this journey not just productive but also genuinely fun.

## Final Thoughts

This whole journey started with an interest in Patient-Level Prediction, and it turned into building the foundations that make PLP possible in JuliaHealth. By contributing to HealthBase.jl and creating OMOPCDMFeasibility.jl, I was able to add some of those missing building blocks that will help future research and development in this space.

For me, GSoC has been both a technical learning experience and a personal milestone. I'm excited to keep contributing to JuliaHealth and to open-source in general.

**If you'd like to connect:** [LinkedIn](https://www.linkedin.com/in/kosuriindu/) | [GitHub](https://github.com/kosuriindu)
