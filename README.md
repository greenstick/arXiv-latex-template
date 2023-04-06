# Meeting Minutes

A log of considerations with respect to the research and writing of this paper.

## 6/4/21
- Updated section structure
- Bring machine learning into line with current literature on quantum kernel methods
- Marked a bunch of comments as resolved

## 5/4/21
- Todo:
    - Simulation of quantum systems & applications
    - Simulation of classical systems & applications
    - New figure for Grover's algorithm (or similar) showing problem instances and compute time (e.g. absolute, operations, or some other time variable) incorporating estimates around overhead from error correction, etc.
    - Advantages in sample complexity & applications
    - Finish marking comments as (keep/discard/table/add/edit) and address straight forward ones
    - Create Git repo for a new `edits` branch
    - Add figure notebooks to Git repo

## 4/14/21

- Consider submitting to a computational journal, rather than one that is purely quantum or biology focused.
    - For example: https://www.journals.elsevier.com/journal-of-computational-science
- Figure 2:
    - Is the figure best realized as a conceptual figure or one based on a model simulating specific dynamics (connectivity, noise, etc.)?
    - We landed on the idea that we'd work to keep the four panel version of figure 2, make clear it's conceptual nature, but also include some basic model that accounts for some of the constant factors to show that an overhead and cross over exist.
    - Alternative approaches could be to discard figure 2 or develop a novel figure with a single graph targeting a well characterized biological use case (this could also be a separate figure to include).
- Sample Complexity Use Cases
    - Sample complexity use case (propose this as a possible area for further research in the paper)
    - The value of a biological/clinical sample, especially in the rare disease context, is >> than most 'big data' samples sourced from web applications, etc.
    - Assuming a polynomial gain in sample complexity (i.e. fewer classical samples required) by the quantum model over a large family of distributions, QML models may have applications to rare disease (e.g. phenotyping/subtyping)
    - A 'no go' result exists, indicating that the sample complexity of quantum and classical learning using quantum examples are equivalent up to constant factors under their respective PAC models if we place no constraints on the sample distribution.
    - However, Servedio and Gortler showed there exists a concept class that is efficiently learnable under the quantum but not classical setting, assuming the hardness of prime factorization. T
    - In a similar vein, the learning of DNF formula w.r.t. the uniform distribution has been shown to yield an exponential reduction in sample complexity (Bshouty and Jackson, 2006). Are there other problems that allow for similar (including polynomial) reductions?
    - Given the >> value of biological/clinical samples, a polynomial time input of classical data may not represent a significant obstacle to gaining a practical advantage in the rare disease context, provided a polynomial or greater reduction in sample complexity is possible. 
    - Gap: 'Are there problems relevant to the rare disease use case for which reductions in sample complexity can be attained?'
- Simulating diffusion dynamics with Q. PDE/ODE approaches
    - Ben will dig into the literature and write a paragraph on this and the biological applications. 
- Trimming paper
    - Section 2: models of complexity and Section 3.2 evidence for theoretical speedups will be moved into an appendix
    - Ben will look to other areas that can be similarly migrated
- Goal to submit to arXiv by June 20 at the latest
- NLM/ITC conference starts June 21

## 3/22/21

- Review:
    - Audience; the paper as currently formed is aiming to address two audiences, with the following questions:
        - Quantum researchers: What are the questions and problems that need to be solved in comp. bio. for which a quantum approach would be valuable? Why?
        - Comp. bio. researchers: How should we be thinking about QC as a methodological tool? Where and when can we expect QC to yield an experimental or operational advantage?
    - Structure; trim down longer sections
        - Complexity section is a bit long, trim it
        - Consider whether subtle points are clarifying or confusing

- Edits discussed:
    - Ben
        - Add in more details around the contemporary problems we are trying to solve in computational biology and their applications. 
        - Add in links between these problems and the different types of quantum advantages (e.g. sample complexity and inherently small samples sizes for orphan diseases). Highlight the motivation for the development of methods to address them.
        - Add in details around input approaches (spin, phase, angle) and learned input models
        - Work on cleaning up complexity section and trimming it
        - Update abstract (including for submission to NLM ITC) to remove claims of killer app/early quantum advantages
    - Nicolas
        - Opinions on quantum simulation (e.g. embedding theories, vibrational problems, etc.)
    - Gian
        - Are there other frameworks like NASA's technological readiness levels that could be relevant that we can leverage?
 
- Papers discussed
    - A variational approach for learning inputs/embeddings: https://arxiv.org/abs/2001.03622
    - Combinatorial approach for inferring (driver) mutation combinations possible for proof of principle numerical simulation paper
        - CPU: https://pubmed.ncbi.nlm.nih.gov/30700767/
        - GPU: https://pubmed.ncbi.nlm.nih.gov/32029803/
    - A fault-tolerant non-Clifford gate for the surface code in two dimensions (https://advances.sciencemag.org/content/6/21/eaay4929.full). This paper entered into the conversation but is not central to the paper we're working on. 
