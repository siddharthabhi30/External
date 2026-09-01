# Career-map

**Siddharth** · [siddharthabhi30@gmail.com](mailto:siddharthabhi30@gmail.com) · [full background](https://sweltering-clematis-24f.notion.site/2ff1e8d5adfd80699d01d220f8d1f8e1?v=3bc1e8d5adfd8057950a000ca8e833b8)

**1 September 2026.** A survey of computational fields, compiled while choosing one to commit to. Sources in §7.

## 0. Background

- **Software engineer, 6 years.** SDE-2 at AWS since 2022 — Athena (distributed SQL query engine) and Lex. Distributed systems: admission control at 3,000+ TPS, resource vending at 2,000+ TPS, consistent hashing, zero-downtime migration of a live counting pathway.
- **Independent coursework.** MIT 6.824 Distributed Systems — full Raft implementation in Go. MIT 6.S081 Operating Systems.
- **Topcoder competitive programming** — global rank 11.
- **Physics-gated ConvLSTM for track-before-detect.** Added a learned bypass gate to prevent saturation when integrating sub-noise targets across frames. On synthetic radar data, detection improved from 83% to 92%. [Write-up](https://medium.com/@siddharthabhi30/when-physics-met-neural-network-67a35670c0c7).
- **Research: high-dimensional particle flow filters, DNN-aided.** Submission planned for ICASSP 2027.

## 1. Purpose of this document

**The decision.** Which technical field to commit to for the next decade.

**What I want from the field.** A place where building the system and doing
research run in parallel, in one job rather than two, and where inventing
something new is a normal part of the work.

**How this survey was built.** Fields are grouped by **how industry hires** — job
title and the requirements text of live postings — not by shared mathematics or
academic subject. Two fields sharing an equation are treated as one only if the
same postings accept both backgrounds. The evidence and source inventory are in
§7; job links may expire after this document's date.

**What I am asking for.** A potential project, a networking lead, or general
career guidance. I am an Indian citizen, so US programmes gated on citizenship
or security clearance are out of scope. Civil, European, Indian and commercial
routes are open.

## 2. Selection criteria

- **Momentum** — the work should build up over ten years, not stay at the level of operating tools.
- **Algorithmic centre** — modelling, inference, optimization or signal processing as the primary activity.
- **An existing application.**
- **Research that advances the work itself** — new methods arising from the engineering problem, not side projects run alongside it.

Not weighted: salary, job volume, prestige, proximity to current skills.
Algorithms and software, not circuit or hardware design. MSc or PhD acceptable.

## 3. Main wave-based lanes: hiring and applications

Shared mathematics does not make these one career. Hiring separates them by
modality and application. Each can support both scientific work and products.

| Measurement and application | Hires as | Requirements and evidence |
|---|---|---|
| Conventional radar; counter-UAS under interference | Radar Signal Processing Engineer | *Detection/estimation, waveforms, phenomenology.* [Measured interference](https://doi.org/10.21227/E47T-P857) · [synchronized drone data](https://www.nature.com/articles/s41597-026-06802-6) · [review](https://doi.org/10.1016/j.cja.2026.104203) |
| Moving-platform SAR; Earth deformation, flood and ice | [SAR Engineer](https://www.iceye.com/careers/positions) · [sarmap](https://www.sarmap.ch/index.php/sar-remote-sensing-specialist/) | *Image formation, radar physics, phenomenology.* [NISAR](https://science.nasa.gov/mission/nisar/) · [Sentinel-1](https://dataspace.copernicus.eu/) · [MintPy](https://github.com/insarlab/MintPy) |
| SAR-GMTI / DMTI; wide-area moving targets | Radar/SAR Moving-Target Engineer | *Moving-target indication and tracking.* [Sandia](https://www.sandia.gov/radar/modes-frequency-bands-of-operation/) · [Gotcha challenge](https://www.sdms.afrl.af.mil/content/challenge_areas/documents/A_challenge_problem_for_SAR-based_GMTI_in_urban_environments.pdf) |
| Underwater acoustics; marine-mammal and offshore monitoring | Sonar / Marine Acoustics Engineer | *Hydrography, geophysics and marine geospatial methods.* [NOAA requirements and data](https://www.fisheries.noaa.gov/topic/offshore-wind-energy/assessing-impacts-to-marine-life) · [Saildrone](https://www.saildrone.com/news/new-acoustic-capabilities-protect-marine-mammals) |
| Seismic/GPR; utilities, voids, tunnels and physical properties | Geophysicist / Subsurface Imaging Engineer | *Wave propagation and numerical optimization.* [SLB](https://apply.slb.com/careers/job/563499733040154-artificial-intelligence-engineer-houston-united-states) · [Exodigo](https://www.exodigo.com/about) · [Twente data](https://research.utwente.nl/en/datasets/ground-penetrating-radar-dataset-with-ground-truth-data-of-utilit/) · [OpenFWI](https://github.com/lanl/OpenFWI) |
| MRI/CT/ultrasound; clinical reconstruction | Reconstruction Scientist | *Applied mathematics, physics and inverse problems.* [Philips](https://philips.wd3.myworkdayjobs.com/jobs-and-careers/job/Best/Reconstruction-Algorithms-Developer---MRI_579237-2) · [fastMRI](https://github.com/facebookresearch/fastMRI) · [DeepInverse](https://github.com/deepinv/deepinv) |
| Optical sensing; wafer inspection and hidden structure | Metrology / Lithography Algorithm Engineer | *Physics-based optical or scattering simulation.* [ARCNL](https://arcnl.nl/jobs/phd-physics-informed-machine-learning-for-semiconductor-metrology-1333971) · [CXIDB](https://www.cxidb.org/) |

## 4. Other lanes surveyed

**Sensing-adjacent**
- Tracking and sensor fusion — [Stone Soup](https://github.com/dstl/Stone-Soup) · [nuScenes](https://www.nuscenes.org/). The postings sampled were predominantly automotive.
- Navigation, localization and SLAM — [OpenVINS](https://github.com/rpng/open_vins) · [GTSAM](https://github.com/borglab/gtsam). Sampled postings emphasised tooling and prior domain experience.
- Physiological and neural inference — [neurotechjobs](https://neurotechjobs.io/) · [MNE-Python](https://mne.tools/stable/). The sampled research roles were predominantly PhD-gated.
- Speech, audio and spatial sound — [beamforming tools](https://github.com/eac-ufsm/beamforming-tools).
- Non-destructive evaluation — industrial ultrasound and guided-wave inspection; its algorithmic branch overlaps computational wave imaging.
- Distributed fibre sensing — [Marlinks/Fluves](https://www.fluves.com/products/marlinks): *"real-time monitoring of subsea power cables using fiber optic sensing"*. [Prisma Photonics](https://www.prismaphotonics.com/careers/) · [OptaSense/Luna](https://www.optasense.com/) · [DASCore](https://github.com/dasdae/dascore) · [vessel detection from a submarine cable, IEEE J-STARS 2026](https://arxiv.org/abs/2509.11614), code released.

**Simulation and design**
- Computational fluid dynamics — ANSYS Fluent, OpenFOAM and [SU2](https://su2code.github.io/). Sampled entry postings focused on tool operation; solver development appeared as a separate tier.
- Computational electromagnetics — CST, HFSS, COMSOL and [MEEP](https://meep.readthedocs.io/). Antenna and device design. Sampled entry postings focused on tool operation; many solver-development roles found were clearance-gated.
- Fusion plasma simulation — [WarpX](https://github.com/ECP-WarpX/WarpX) · [BOUT++](https://github.com/boutproject/BOUT-dev). Gyrokinetic and PIC codes at Thea, Proxima and Commonwealth Fusion. All postings in this sample were research-level.
- [Climate and Earth-system modelling](https://www.ecmwf.int/en/about/jobs).
- Numerical solvers and simulators — [Devito](https://github.com/devitocodes/devito) · [FEniCS](https://fenicsproject.org/).

**Communications and information**
- Wireless PHY and modem — [Sionna](https://github.com/NVlabs/sionna) · [OpenAirInterface](https://github.com/OPENAIRINTERFACE/openairinterface5g). LDPC and Polar codes, channel estimation and 3GPP systems.

## 5. Momentum proof from requirements text

| Lane | Early-career evidence | Senior evidence | What accumulates |
|---|---|---|---|
| Radar | [NTU Research Engineer I](https://ntu.wd3.myworkdayjobs.com/en-US/Careers/job/Research-Engineer-I--Radar-_R00023060): experimental sensing, waveform/array processing and evaluation | [Rivian Staff Radar DSP](https://careers.rivian.com/careers-home/jobs/32119): raw ADC to 4-D detections, MIMO architecture, super-resolution, interference, tracking and real-time implementation | Sensor phenomenology, failure diagnosis and architecture trade-offs |
| Seismic / subsurface | [SLB entry-level GeoSolutions](https://careers.slb.com/jobdescription.aspx?id=EF18051-en_US+1): process 3-D/4-D seismic data, migration, velocity-model building and QC | [SLB FWI & AI Scientist](https://careers.slb.com/jobdescription.aspx?id=EF16555-en_US+1): design FWI foundation models, learned regularization, cycle-skipping mitigation and GPU/HPC methods | Wave physics, inversion failure diagnosis and production-scale scientific judgment |

The delta is not merely years or a newer framework. The senior role owns which
physical assumptions can be trusted and what to change when the system fails.

## 6. Current lean

Leaning towards **physics-based remote sensing and inversion** — recovering
physical state at a distance from measured waves. Not settled.


## 7. Sources by lane

**Radar** — Jobs: [Sandia radar/ISR](https://www.sandia.gov/radar/jobs/) · [Helsing](https://jobs.accel.com/companies/helsing-2/jobs/39131980-ai-research-engineer-signal-processing) · [Array Labs](https://jobs.lever.co/arraylabs.io/56d997f8-4c3a-4a71-beb7-f488782652a0) · [MathWorks radar/phased array](https://www.mathworks.com/company/jobs/opportunities/34757-software-engineer-radar-and-phased-array-systems) · [Rivian radar DSP](https://careers.rivian.com/careers-home/jobs/32119) · [Poland raw-IQ radar](https://jobs.ashbyhq.com/rnrs.solutions/8e19b8b0-9b65-4d83-9a38-024d5a344ddf) · [Data Patterns India](https://www.datapatternsindia.com/careers/openings.php?id=781) · [Sensata Pune](https://sensata.wd1.myworkdayjobs.com/en-US/Sensata-Careers/job/Radar-Embedded-Firmware-Engineer_IRC97078) · [NTU Singapore](https://ntu.wd3.myworkdayjobs.com/en-US/Careers/job/Research-Engineer-I--Radar-_R00023060) · [AeroVect radar perception](https://jobs.ashbyhq.com/aerovect/a245c891-e718-4976-b85c-5a5020788102) · [Applied Physical Sciences](https://aphysci.com/careers/).
Data: [measured 77-GHz FMCW interference](https://doi.org/10.21227/E47T-P857) · [2026 synchronized drone FMCW/CW/RF](https://doi.org/10.1038/s41597-026-06802-6) · [RADIal](https://github.com/valeoai/RADIal) · [RaDICaL](https://databank.illinois.edu/datasets/IDB-3289560) · [ColoRadar](https://doi.org/10.1177/02783649211068535) · [CARRADA](https://github.com/valeoai/carrada_dataset) · [RadarScenes](https://radar-scenes.com/) · [77 GHz drone/bird/human](https://zenodo.org/records/5845259/latest) · [AERPAW RF-UAV TDOA](https://doi.org/10.5061/dryad.vq83bk44h) · [BLE raw-IQ AoA](https://zenodo.org/records/15424721) · [ARIM-v2](https://github.com/ristea/arim-v2) · [awesome-radar-perception](https://github.com/Radar-Camera-Fusion/Awesome-Radar-Perception).
PhD: [Aalborg UAS radar](https://www.vacancies.aau.dk/phd-positions/show-vacancy/vacancyId/954014) · [TU Delft vehicular radar](https://euraxess.ec.europa.eu/jobs/157738) · [Luxembourg 4D MIMO imaging](https://www.uni.lu/en/jobs/phd-candidate-for-radar-based-4d-imaging-with-advanced-massive-mimo-signal-processing/) · [CEA EM signature + AI](https://instn.cea.fr/en/these/electromagnetic-signature-modeling-and-ai-for-radar-object-recognition/) · [CWI — inverse problems for wave-based imaging](https://www.cwi.nl/nl/werken-bij/vacatures/1332446/). Learning: [MIT Intro to Radar](https://www.youtube.com/watch?v=Hw5IaS6-Fzw).
Current state of the field: [Radar signal processing based on AI — a comprehensive review of developments, trends and challenges](https://doi.org/10.1016/j.cja.2026.104203) (Chinese Journal of Aeronautics, 2026). Covers waveform design, detection, recognition, tracking, clutter and jamming suppression, imaging, and the hardware for deployment. Proposed remedies include algorithm unfolding, physics-guided networks and physics-based simulation, alongside self-supervision, adaptation and model compression. Two open problems it states are non-stationary, non-Gaussian sea clutter, for which no fixed statistical model holds, and the mismatch between a low-dimensional kinematic state and a high-dimensional scattering signature.

**SAR** — Jobs: [ICEYE](https://www.iceye.com/careers/positions) · [Capella](https://www.capellaspace.com/careers) · [Synspective image-processing engineer](https://careers.synspective.com/o/sar-image-processing-engineer) · [Array Labs image formation/reconstruction](https://jobs.lever.co/arraylabs.io/56d997f8-4c3a-4a71-beb7-f488782652a0) · [Array Labs MTI/STAP](https://jobs.lever.co/arraylabs.io/05950462-f9f1-4736-86c3-aea60e97c45f) · [MathWorks SAR](https://www.mathworks.com/company/jobs/opportunities/36842-senior-radar-signal-processing-engineer-sar) · [DLR careers](https://www.dlr.de/en/careers/jobs) · [Sandia radar/ISR](https://www.sandia.gov/radar/jobs/) · [NORCE InSAR](https://www.egu.eu/jobs/7924/researchersenior-researcher-insar-development-and-applications/) · [Saab MSc thesis, SciML for inverse problems in SAR](https://www.saab.com/career/job-opportunities/masters-thesis-30-45-hp-scientific-machine-learning-for-physics-informed-inverse-problems-in-sar-imaging1).
Data: [NISAR](https://science.nasa.gov/mission/nisar/) · [Copernicus/Sentinel-1](https://dataspace.copernicus.eu/) · [ASF DAAC](https://asf.alaska.edu/) · [ASF coherence/backscatter](https://asf.alaska.edu/datasets/daac/global-seasonal-sentinel-1-interferometric-coherence-and-backscatter-dataset/) · [Capella open data](https://support.capellaspace.com/how-do-i-access-capellas-open-data) · [Umbra open data](https://umbra.space/open-data/) · [100-image SLC stack](https://zenodo.org/records/12189041) · [BigEarthNet](https://bigearth.net/) · [Gotcha raw phase history](https://www.sdms.afrl.af.mil/index.php?collection=gotcha) · [Gotcha SAR-GMTI](https://www.sdms.afrl.af.mil/content/challenge_areas/documents/A_challenge_problem_for_SAR-based_GMTI_in_urban_environments.pdf) · [UNICORN airborne SAR/EO](https://github.com/AFRL-RY/data-unicorn-2008) · [Sandia complex SAR](https://www.sandia.gov/radar/pathfinder-radar-isr-and-synthetic-aperture-radar-sar-systems/complex-data-clone/) · [AFRL ADTS](https://www.sdms.afrl.af.mil/index.php?collection=adts) · [BELSAR](https://www.nature.com/articles/s41597-024-03320-1).
India: [GalaxEye](https://galaxeye.space/) launched [Drishti](https://www.eoportal.org/satellite-missions/galaxeye), carrying SAR and a multispectral imager on one platform, May 2026. Its [AI posting](https://careers.galaxeye.space/jobs/Careers) asks for *"PyTorch, Vision Transformers, Diffusion Models, GANs, VAEs, CLIP, BLIP, LLaVA"* and lists no radar physics.
Code: [ISCE2](https://github.com/isce-framework/isce2) · [ISCE3](https://github.com/isce-framework/isce3) · [MintPy](https://github.com/insarlab/MintPy) · [pyroSAR](https://github.com/johntruckenbrodt/pyroSAR) · [awesome-sar](https://github.com/RadarCODE/awesome-sar) · [NGA SarPy](https://github.com/ngageoint/sarpy) · [RITSAR](https://github.com/dm6718/ritsar) · [AISTAP-SIM](https://github.com/mit-ll/AISTAP-SIM).
Research directions currently funded: distributed radar interferometry and tomography with smallsat clusters, blind source separation for spaceborne SAR, InSAR denoising, stochastic signal processing for SAR ([DLR](https://www.dlr.de/en/hr/)); InSAR for infrastructure ([PoliMi](https://www.polimi.it/en/phd/prospective-phd-candidates/admission/calls-and-open-positions/ciclo-42/2nd-call)); multi-temporal InSAR — time series analysis, phase unwrapping, atmospheric and ionospheric correction ([NORCE](https://www.egu.eu/jobs/7924/researchersenior-researcher-insar-development-and-applications/)) · [SAR tomography review](https://www.tandfonline.com/doi/10.1080/10095020.2025.2510365) · [NASA SAR introduction and training](https://www.earthdata.nasa.gov/learn/trainings/introduction-synthetic-aperture-radar-sar-its-applications) · [SAR-CBC learning resources, UAF](https://learnsar.open.uaf.edu/sar-resources/) · [NASA free SAR semester](https://science.nasa.gov/mission/nisar/sar-education-resources/).

**Sonar / marine acoustics** — Jobs: [Kongsberg](https://www.kongsberg.com/careers/vacancies/software-developer/) · [General Dynamics undersea acoustics](https://www.gd.com/careers/chief-engineer-undersea-acoustic-systems-manassas-va-us-2026-72754-gdms-opportunity) · [Lobster Robotics](https://www.lobster-robotics.com/careers) · [Aquabyte — underwater perception](https://jobs.lever.co/aquabyte) · [MIT Media Lab underwater acoustics](https://www.media.mit.edu/posts/postdoc-underwater-acoustic-systems/) · [ARL:UT postdocs](https://wwwext.arlut.utexas.edu/postdocs.shtml) · [ASA positions](https://acousticalsociety.org/phd-and-post-doctoral-research-positions/).
Data/code: [NOAA passive acoustic archive](https://www.ncei.noaa.gov/products/passive-acoustic-data) · [NOAA water-column sonar](https://www.ncei.noaa.gov/products/water-column-sonar-data) · [arlpy](https://github.com/org-arl/arlpy) · [UnderwaterAcoustics.jl](https://github.com/org-arl/UnderwaterAcoustics.jl) · [Acoular](https://github.com/acoular/acoular) · [pyroomacoustics](https://github.com/LCAV/pyroomacoustics).
Learning: [MIT Computational Ocean Acoustics](https://ocw.mit.edu/courses/2-068-computational-ocean-acoustics-13-853-spring-2003/pages/lecture-notes/) · [MIT Acoustical Oceanography](https://ocw.mit.edu/courses/2-682-acoustical-oceanography-spring-2012/) · [MIT–WHOI AOPE](https://mit.whoi.edu/academics/fields/aope/aope-areas-of-study/).
**Seismic / subsurface** — Jobs: [SLB FWI+AI](https://apply.slb.com/careers/job/563499733040154-artificial-intelligence-engineer-houston-united-states) · [BRGM seismic research engineer](https://brgm-recrute.talent-soft.com/job/emploi-ingenieur-chercheur-geophysicien-methodes-sismiques-f-h-_4052.aspx?LCID=2057) · [Exodigo](https://www.exodigo.com/about) · [RodRadar](https://rodradar.com/).
Data/code: [OpenFWI](https://github.com/lanl/OpenFWI) · [Devito](https://github.com/devitocodes/devito) · [gprMax](https://github.com/gprMax/gprMax) · [Twente field GPR, CC0](https://research.utwente.nl/en/datasets/ground-penetrating-radar-dataset-with-ground-truth-data-of-utilit/).
PhD/learning: [ETH reflection seismology for CO₂ storage](https://www.egu.eu/jobs/7669/phd-position-in-reflection-seismology-for-carbon-capture-and-sequestration/) · [CWI inverse problems for wave-based imaging](https://www.cwi.nl/nl/werken-bij/vacatures/1332446/) · [Colorado School of Mines](https://gradprograms.mines.edu/program/geophysics-and-geophysical-engineering/) · [Coursera: Computers, Waves, Simulations](https://www.coursera.org/learn/computers-waves-simulations).
Research: [2026 computational wave-imaging survey](https://arxiv.org/abs/2410.08329) spanning seismic, NDT and ultrasound · [DLM-FWI](https://doi.org/10.1093/gji/ggag019), which adds a learned matching filter to wave-equation inversion to reduce cycle-skipping, tested on synthetic and Volve field data.

**Medical reconstruction** — Jobs: [Philips MRI recon](https://philips.wd3.myworkdayjobs.com/jobs-and-careers/job/Best/Reconstruction-Algorithms-Developer---MRI_579237-2) · [GE recon physics](https://gehc.wd5.myworkdayjobs.com/en-US/GEHC_ExternalSite/job/Senior-Research-Scientist---Reconstruction-Physics_R4044564-1) · [Canon CT recon](https://www.research.us.medical.canon/opportunities/sr-ct-reconstruction-scientist/) · [ISMRM career centre](https://www.ismrm.org/career-center/faculty-positions/).
Data/code: [fastMRI raw k-space](https://github.com/facebookresearch/fastMRI) · [Low-Dose CT challenge](https://www.aapm.org/grandchallenge/lowdosect/) · [Cancer Imaging Archive](https://www.cancerimagingarchive.net/) · [DeepInverse](https://github.com/deepinv/deepinv) · [BART](https://github.com/mrirecon/bart) · [ASTRA](https://github.com/astra-toolbox/astra-toolbox) · [CIL](https://github.com/TomographicImaging/CIL).
Learning: [Cambridge DAMTP inverse problems notes](https://www.damtp.cam.ac.uk/research/cia/files/teaching/Inverse_Problems_2020/LectureNotes2020.pdf) · [CIBM reconstruction tutorial](https://cibm.ch/tutorial-may-2020-icassp/).

**Metrology** — [ASML physics-informed ML scientist](https://www.asml.com/en/careers/find-your-job/machine-learning-scientist-physics-j00345223) · [ARCNL PhD](https://arcnl.nl/jobs/phd-physics-informed-machine-learning-for-semiconductor-metrology-1333971) · [AIM Solutions phase retrieval](https://jobs.ashbyhq.com/aim-solutions/1cc9e6fa-b23f-4cd4-a948-5e00d96fb9b9) · [Intel mask metrology](https://intel.wd1.myworkdayjobs.com/en-US/External/job/Image-Processing-Engineer--C---Linux-_JR0285764) · [CXIDB coherent diffraction data](https://www.cxidb.org/) · [inverse lithography review](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12287475/).

**Tracking / counter-UAS** — Jobs: [Anduril sensor fusion](https://job-boards.greenhouse.io/andurilindustries/jobs/5194560007) · [9 Mothers, perception](https://jobs.ashbyhq.com/9-mothers/fd8c2655-efe2-490e-bff8-e8fed5dbf9aa) · [Allen Control Systems](https://jobs.ashbyhq.com/allen-control-systems/6eca9cbe-1a43-4082-91a5-84871e056637) · [Applied Intuition](https://jobs.ashbyhq.com/applied/47aa4ad5-62c0-4aba-b414-b60820029ced/) · [MathWorks fusion/tracking](https://www.mathworks.com/company/jobs/opportunities/28071-sensor-fusion-and-tracking-software-engineer).
Data/code: [Anti-UAV challenge](https://anti-uav.github.io/dataset/) · [Stone Soup (DSTL)](https://github.com/dstl/Stone-Soup) · [AB3DMOT](https://github.com/xinshuoweng/AB3DMOT) · [nuScenes](https://www.nuscenes.org/) · [Argoverse](https://www.argoverse.org/) · [MTT course](https://mtt.edu.hendeby.se/about/).

**Fibre sensing (DAS)** — [Prisma Photonics DSP researcher](https://www.prismaphotonics.com/careers/) · [DASCore](https://github.com/dasdae/dascore) · [DAS event dataset](https://www.nature.com/articles/s41597-025-05088-4) · [vessel detection on submarine cable](https://arxiv.org/pdf/2509.11614) · [silent whales via seabed fibre (PNAS)](https://www.pnas.org/doi/abs/10.1073/pnas.2603077123) · [Arctic cable: whales, storms, ships, quakes](https://www.nature.com/articles/s41598-022-23606-x) · [ML benchmarking for DAS](https://arxiv.org/pdf/2503.20681).

**Wireless PHY** — [Sionna (NVIDIA)](https://github.com/NVlabs/sionna) · [OpenAirInterface](https://github.com/OPENAIRINTERFACE/openairinterface5g) · [GNU Radio](https://www.gnuradio.org/) · [Apple 6G modem](https://jobs.anitab.org/companies/apple/jobs/73763574-wireless-systems-engineer-6g-cellular-modem) · [Intel DSP algorithms](https://intel.wd1.myworkdayjobs.com/External/job/Virtual-US/Senior-DSP-Algorithm-Engineer_JR0281792) · [MIT 6.450](https://ocw.mit.edu/courses/6-450-principles-of-digital-communications-i-fall-2006/resources/lecture-1-introduction/) · [deep unfolding for wireless review](https://arxiv.org/html/2502.05952).
