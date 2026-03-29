# Awesome MAPF Resources

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT) ![RRs](https://img.shields.io/badge/PRs-welcome-brightgreen)

<img src="./assets/mapf_demo_500.svg" width="100%" alt="Map created using pogema(https://github.com/Cognitive-AI-Systems/pogema). The solver is LaCAM(https://arxiv.org/abs/2211.13432).">


---

A list aiming to broadly cover excellent papers, repositories, websites, and videos related to Multi-Agent Pathfinding (MAPF)

Contributions welcome! Feel free to open a Pull-requests!

> Note : If you find any typos or incorrect information, I'd greatly appreciate it if you could report them through Issues, Pull-requests or other Contact Methods.　&#x1F64F;

## Contents

MAPF is the problem of computing optimal, collision-free paths for multiple agents from their start positions to their respective goals in a shared environment. 

- [Papers](#papers)
    - [Survey](#survey)
    - [Search-based Approach](#search-based-approach)
    - [Sampling-based Approach](#sampling-based-approach)
    - [Learning-based Approach](#learning-based-approach)
    - [Hybrid Approach](#hybrid-approach)
    - [Collision Resolution](#collision-resolution)
- [Repositories](#repositories)
    - [Solver Implementations](#solver-implementations)
        - [Search](#search)
        - [CBS Family](#cbs-family)
        - [LaCAM Family](#lacam-family)
        - [LNS Family](#lns-family)
        - [Collision Resolution](#collision-resolution-1)
        - [Learning-based](#learning-based)
        - [Hybrid](#hybrid)
        - [Others](#others)
    - [Benchmarks & Visualization Tools & Testbed](#benchmarks--visualization-tools--testbed)
- [Websites](#websites)
- [Videos](#videos)

## Papers　&#x1f4d6;

### Survey

**Multi-Agent Path Finding – An Overview** \
Roni Stern \
2019, [[ResearchGate](https://www.researchgate.net/publication/336611576_Multi-Agent_Path_Finding_-_An_Overview)] 

**Multi-Agent Pathfinding: Definitions, Variants, and Benchmarks** \
Roni Stern, Nathan Sturtevant, Ariel Felner, Sven Koenig, Hang Ma, Thayne Walker, Jiaoyang Li, Dor Atzmon, Liron Cohen, T. K. Satish Kumar, Eli Boyarski, Roman Bartak \
2019, [[arXiv](https://arxiv.org/abs/1906.08291)] 

**Problem Compilation for Multi-Agent Path Finding: a Survey** \
Pavel Surynek \
2022, [[IJCAI](https://www.ijcai.org/proceedings/2022/783)] [[video](https://www.ijcai.org/proceedings/2022/video/783)] 

**A Comprehensive Review on Leveraging Machine Learning for Multi-Agent Path Finding** \
Jean-Marc Alkazzi, Keisuke Okumura \
2024, [[ResearchGate](https://www.researchgate.net/publication/380014238_A_Comprehensive_Review_on_Leveraging_Machine_Learning_for_Multi-Agent_Path_Finding)] 

**Where Paths Collide: A Comprehensive Survey of Classic and Learning-Based Multi-Agent Pathfinding** \
Shiyue Wang, Haozheng Xu, Yuhan Zhang, Jingran Lin, Changhong Lu, Xiangfeng Wang, Wenhao Li \
2025, [[arXiv](https://arxiv.org/abs/2505.19219)] 


### Search-based Approach

**Finding Optimal Solutions to Cooperative Pathfinding Problems** \
Trevor Standley \
2010, [[AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/7564)] [[code](https://github.com/Urist/CooperativePathfinding?tab=readme-ov-file)]

**Conflict-based search for optimal multi-agent pathfinding** (CBS)\
Guni Sharon, Roni Stern, Ariel Felner, Nathan R. Sturtevant \
2015, [[ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0004370214001386)] [[code](https://github.com/whoenig/libMultiRobotPlanning)]

**Suboptimal Variants of the Conflict-Based Search Algorithm for the Multi-Agent Pathfinding Problem** (ECBS)\
Max Barer, Guni Sharon, Roni Stern, Ariel Felner \
2015, [[AAAI](https://ojs.aaai.org/index.php/SOCS/article/view/18315)] [[code](https://github.com/whoenig/libMultiRobotPlanning)]

**ICBS: Improved Conflict-Based Search Algorithm for Multi-Agent Pathfinding** (ICBS) \
Eli Boyarski, Ariel Felner, Roni Stern, Guni Sharon, Oded Betzalel, David Tolpin, Eyal Shimony \
2015, [[AAAI](https://ojs.aaai.org/index.php/SOCS/article/view/18343)] [[code](https://github.com/gloriyo/MAPF-ICBS)]

**Subdimensional expansion for multirobot path planning** (M\*)\
Glenn Wagner, Howie Choset \
2015, [[ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0004370214001271)] [[video](https://www.youtube.com/watch?v=pfeBNvOqzvE)] [[code](https://github.com/rap-lab-org/public_cppmomapf)]

**Searching with Consistent Prioritization for Multi-Agent Path Finding** (PBS)\
Hang Ma, Daniel Harabor, Peter J. Stuckey, Jiaoyang Li, Sven Koenig \
2018, [[arXiv](https://arxiv.org/abs/1812.06356)] [[code](https://github.com/Jiaoyang-Li/PBS)]

<**Disjoint Splitting for Multi-Agent Path Finding with Conflict-Based Search** (CBS with disjoint splitting)\
Jiaoyang Li, Daniel Harabor, Peter J. Stuckey, Ariel Felner, Hang Ma, Sven Koenig \
2019, [[AAAI](https://ojs.aaai.org/index.php/ICAPS/article/view/3487)]

**Improved Heuristics for Multi-Agent Path Finding with Conflict-Based Search** (CBSH2)\
Jiaoyang Li, Ariel Felner, Eli Boyarski, Hang Ma, Sven Koenig \
2019, [[IJCAI](https://www.ijcai.org/proceedings/2019/63)] [[code](https://github.com/Jiaoyang-Li/CBSH2)]


**Multi-Agent Pathfinding with Continuous Time** (CCBS) \
Anton Andreychuk, Konstantin Yakovlev, Dor Atzmon, Roni Stern \
2019, [[arXiv](https://arxiv.org/abs/1901.05506)] [[code](https://github.com/PathPlanning/Continuous-CBS)]

**EECBS: A Bounded-Suboptimal Search for Multi-Agent Path Finding** (EECBS)\
Jiaoyang Li, Wheeler Ruml, Sven Koenig \
2021, [[DOI](https://doi.org/10.1609/aaai.v35i14.17466)] [[code](https://github.com/Jiaoyang-Li/EECBS)]

**Pairwise Symmetry Reasoning for Multi-Agent Path Finding Search** (CBSH2-RTC) \
Jiaoyang Li, Daniel Harabor, Peter J. Stuckey, Sven Koenig \
2021, [[arXiv](https://arxiv.org/abs/2103.07116)] [[code](https://github.com/Jiaoyang-Li/CBSH2-RTC?tab=readme-ov-file)]

**Anytime Multi-Agent Path Finding via Large Neighborhood Search** (MAPF-LNS) \
Jiaoyang Li, Zhe Chen, Daniel Harabor, Peter J. Stuckey and Sven Koenig1 \
2021, [[IJCAI](https://www.ijcai.org/proceedings/2021/568)] [[code](https://github.com/Jiaoyang-Li/MAPF-LNS)]

**MAPF-LNS2: Fast Repairing for Multi-Agent Path Finding via Large Neighborhood Search** (MAPF-LNS2)\
Jiaoyang Li, Zhe Chen, Daniel Harabor, Peter J. Stuckey, Sven Koenig \
2022, [[AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/21266)] [[code](https://github.com/Jiaoyang-Li/MAPF-LNS2)]

**LaCAM: Search-Based Algorithm for Quick Multi-Agent Pathfinding** (LaCAM)\
Keisuke Okumura \
2022, [[arXiv](https://arxiv.org/abs/2211.13432)] [[website](https://kei18.github.io/lacam/)] [[code](https://github.com/Kei18/lacam)]

**Improving LaCAM for Scalable Eventually Optimal Multi-Agent Pathfinding** (LaCAM\*)\
Keisuke Okumura \
2023, [[arXiv](https://arxiv.org/abs/2305.03632)] [[website](https://kei18.github.io/lacam2/)] [[code](https://github.com/Kei18/lacam2)]

**db-LaCAM: Fast and Scalable Multi-Robot Kinodynamic Motion Planning with Discontinuity-Bounded Search and Lightweight MAPF** (db-LaCAM) \
Akmaral Moldagalieva, Keisuke Okumura, Amanda Prorok, Wolfgang Hönig \
2026, [[arXiv](https://arxiv.org/abs/2512.06796)] [[video](https://www.youtube.com/watch?v=K7xUFpH7a48)] [[code](https://github.com/IMRCLab/db-lacam)]


### Sampling-based Approach

**Multi-agent RRT\*: Sampling-based Cooperative Pathfinding (Extended Abstract)** (Multi-agent RRT\*)\
Michal Čáp, Peter Novák, Jiří Vokřínek, Michal Pěchouček \
2013, [[arXiv](https://arxiv.org/abs/1302.2828)] 

**Cooperative Pathfinding Based on Memory-Efficient Multi-Agent RRT\*** (MA-RRT\*FN)\
Jinmingwu Jiang, Kaigui Wu \
2020, [[arXiv](https://arxiv.org/abs/1911.03927)]

**Representation-Optimal Multi-Robot Motion Planning using Conflict-Based Search** (CBS-MP) \
Irving Solis, Read Sandström, James Motes, Nancy M. Amato \
2020, [[arXiv](https://arxiv.org/abs/1909.13352)] [[code](https://github.com/aria-systems-group/Multi-Robot-OMPL)]

**Conflict-based Search for Multi-Robot Motion Planning with Kinodynamic Constraints** (K-CBS) \
Justin Kottinger, Shaull Almagor, Morteza Lahijanian \
2022, [[arXiv](https://arxiv.org/abs/2207.00576)] [[code](https://github.com/IMRCLab/Kinodynamic-Conflict-Based-Search)]


### Learning-based Approach

**PRIMAL: Pathfinding via Reinforcement and Imitation Multi-Agent Learning** (PRIMAL) \
Guillaume Sartoretti, Justin Kerr, Yunfei Shi, Glenn Wagner, T. K. Satish Kumar, Sven Koenig, Howie Choset \
2019, [[arXiv](https://arxiv.org/abs/1809.03531)] [[code](https://github.com/gsartoretti/PRIMAL)]

**PRIMAL2: Pathfinding via Reinforcement and Imitation Multi-Agent Learning -- Lifelong** (PRIMAL2) \
Mehul Damani, Zhiyao Luo, Emerson Wenzel, Guillaume Sartoretti \
2020, [[arXiv](https://arxiv.org/abs/2010.08184)] [[code](https://github.com/marmotlab/PRIMAL2)]

**Message-Aware Graph Attention Networks for Large-Scale Multi-Robot Path Planning** (MAGAT)\
Qingbiao Li, Weizhe Lin, Zhe Liu, Amanda Prorok \
2021, [[arXiv](https://arxiv.org/abs/2011.13219)] [[code](https://github.com/proroklab/magat_pathplanning)]

**CTRMs: Learning to Construct Cooperative Timed Roadmaps for Multi-agent Path Planning in Continuous Spaces** (CTRM) \
Keisuke Okumura, Ryo Yonetani, Mai Nishimura, Asako Kanezaki \
2022, [[arXiv](https://arxiv.org/abs/2201.09467)] [[website](https://omron-sinicx.github.io/ctrm/)] [[code](https://github.com/omron-sinicx/ctrm)]

**SCRIMP: Scalable Communication for Reinforcement- and Imitation-Learning-Based Multi-Agent Pathfinding** (SCRIMP)\
Yutong Wang, Bairan Xiang, Shinan Huang, Guillaume Sartoretti \
2023, [[arXiv](https://arxiv.org/abs/2303.00605)] [[code](https://github.com/marmotlab/SCRIMP)]

**MAPF-GPT: Imitation Learning for Multi-Agent Pathfinding at Scale** (MAPF-GPT)\
Anton Andreychuk, Konstantin Yakovlev, Aleksandr Panov, Alexey Skrynnik \
2024, [[arXiv](https://arxiv.org/abs/2409.00134)] [[website](https://sites.google.com/view/mapf-gpt/)] [[code](https://github.com/CognitiveAISystems/MAPF-GPT)]

**Advancing Learnable Multi-Agent Pathfinding Solvers with Active Fine-Tuning** (MAPF-GPT-DDG)\
Anton Andreychuk, Konstantin Yakovlev, Aleksandr Panov, and Alexey Skrynnik \
2025, [[arXiv](https://arxiv.org/abs/2506.23793)] [[website](https://sites.google.com/view/mapf-gpt-ddg)] [[code](https://github.com/Cognitive-AI-Systems/MAPF-GPT-DDG)]


**Pairwise is Not Enough: Hypergraph Neural Networks for Multi-Agent Pathfinding** (HMAGAT)\
Rishabh Jain, Keisuke Okumura, Michael Amir, Pietro Lio, Amanda Prorok \
2025, [[arXiv](https://arxiv.org/abs/2602.06733)] [[code](https://github.com/proroklab/hmagat)]


### Hybrid Approach

**Learning to Resolve Conflicts for Multi-Agent Path Finding with Conflict-Based Search** (ML-guided CBS)\
Taoan Huang, Sven Koenig, Bistra Dilkina \
2021, [[arXiv](https://arxiv.org/abs/2012.06005)] 

**Quick Multi-Robot Motion Planning by Combining Sampling and Search** (SSSP) \
Keisuke Okumura, Xavier Défago \
2022, [[arXiv](https://arxiv.org/abs/2203.00315)] [[website](https://kei18.github.io/sssp/)] [[video](https://www.youtube.com/watch?v=ZMjrQCKS6Fw&t=75s)] [[code](https://github.com/Kei18/sssp)]


**LNS2+RL: Combining Multi-agent Reinforcement Learning with Large Neighborhood Search in Multi-agent Path Finding** (LNS2+RL)\
Yutong Wang, Tanishq Duhan, Jiaoyang Li, Guillaume Sartoretti \
2025, [[arXiv](https://arxiv.org/abs/2405.17794)] [[code](https://github.com/marmotlab/LNS2-RL)]

**Graph Attention-Guided Search for Dense Multi-Agent Pathfinding** (LaGAT)\
Rishabh Jain, Keisuke Okumura, Michael Amir, Amanda Prorok \
2026, [[arXiv](https://arxiv.org/abs/2510.17382)] [[code](https://github.com/proroklab/lagat)]


### Collision Resolution

**Priority Inheritance with Backtracking for Iterative Multi-agent Path Finding** (PIBT) \
Keisuke Okumura, Manao Machida, Xavier Défago, Yasumasa Tamura \
2019, [[IJCAI](https://www.ijcai.org/proceedings/2019/76)] [[website](https://kei18.github.io/pibt2/)] [[video](https://www.youtube.com/watch?v=8Yrwd0t0NEw&t=4s)] [[code](https://github.com/Kei18/pibt2)]

**Lifelong Multi-Agent Path Finding in Large-Scale Warehouses** (RHCR) \
Jiaoyang Li, Andrew Tinka, Scott Kiesel, Joseph W. Durham, T. K. Satish Kumar, Sven Koenig \
2021, [[AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/17344)] [[code](https://github.com/Jiaoyang-Li/RHCR)]


## Repositories　&#x1f4c1;
The GitHub star list is available [here](https://github.com/stars/romanohu/lists/mapf)

### Solver Implementations

#### Search
| Solver / Repository | Implementation | Description |
| --- | --- | --- |
| M* | [rap-lab-org/public_cppmomapf](https://github.com/rap-lab-org/public_cppmomapf) | C++ implementation based on M* (subdimensional expansion). |
| PBS | [Jiaoyang-Li/PBS](https://github.com/Jiaoyang-Li/PBS) | Reference implementation of PBS for priority-based MAPF search. |

#### CBS Family
| Solver / Repository | Implementation | Description |
| --- | --- | --- |
| CBS / ECBS (library) | [whoenig/libMultiRobotPlanning](https://github.com/whoenig/libMultiRobotPlanning) | Widely used C++ planning library including CBS, ECBS, SIPP, and related planners. |
| ICBS | [gloriyo/MAPF-ICBS](https://github.com/gloriyo/MAPF-ICBS) | Educational and experimental implementation of Improved CBS. |
| CBSH2 | [Jiaoyang-Li/CBSH2](https://github.com/Jiaoyang-Li/CBSH2) | CBS variant with improved high-level heuristics. |
| CCBS | [PathPlanning/Continuous-CBS](https://github.com/PathPlanning/Continuous-CBS) | Continuous-time extension of CBS with time-aware collision handling. |
| EECBS | [Jiaoyang-Li/EECBS](https://github.com/Jiaoyang-Li/EECBS) | Bounded-suboptimal CBS using Explicit Estimation Search. |
| CBSH2-RTC | [Jiaoyang-Li/CBSH2-RTC](https://github.com/Jiaoyang-Li/CBSH2-RTC) | CBSH2 extension with pairwise symmetry reasoning. |
| K-CBS | [IMRCLab/Kinodynamic-Conflict-Based-Search](https://github.com/IMRCLab/Kinodynamic-Conflict-Based-Search) | CBS-style solver for kinodynamic multi-robot planning. |

#### LaCAM Family
| Solver / Repository | Implementation | Description |
| --- | --- | --- |
| LaCAM | [Kei18/lacam](https://github.com/Kei18/lacam) | Fast search-based MAPF solver focused on runtime efficiency. |
| LaCAM* | [Kei18/lacam2](https://github.com/Kei18/lacam2) | LaCAM extension with stronger eventual optimality properties. |
| LaCAM3 | [Kei18/lacam3](https://github.com/Kei18/lacam3) | Engineering-focused LaCAM* extension for real-time and large-scale scenarios. |
| pylacam | [Kei18/pylacam](https://github.com/Kei18/pylacam) | Minimal Python implementation of LaCAM*. |
| db-LaCAM | [IMRCLab/db-lacam](https://github.com/IMRCLab/db-lacam) | Kinodynamic planning pipeline using discontinuity-bounded search plus lightweight MAPF. |

#### LNS Family
| Solver / Repository | Implementation | Description |
| --- | --- | --- |
| MAPF-LNS | [Jiaoyang-Li/MAPF-LNS](https://github.com/Jiaoyang-Li/MAPF-LNS) | LNS-based anytime MAPF solver with iterative repair. |
| MAPF-LNS2 | [Jiaoyang-Li/MAPF-LNS2](https://github.com/Jiaoyang-Li/MAPF-LNS2) | Faster repair-focused successor to MAPF-LNS. |

#### Collision Resolution
| Solver / Repository | Implementation | Description |
| --- | --- | --- |
| PIBT | [Kei18/pibt2](https://github.com/Kei18/pibt2) | Official-style PIBT implementation widely used in lifelong MAPF. |
| pypibt | [Kei18/pypibt](https://github.com/Kei18/pypibt) | Minimal Python implementation of PIBT. |
| Guided-PIBT | [nobodyczcz/Guided-PIBT](https://github.com/nobodyczcz/guided-pibt) | Traffic-flow-guided PIBT extension for lifelong MAPF. |
| RHCR | [Jiaoyang-Li/RHCR](https://github.com/Jiaoyang-Li/RHCR) | Rolling-horizon method for large-scale lifelong MAPF. |

#### Learning-based
| Solver / Repository | Implementation | Description |
| --- | --- | --- |
| PRIMAL | [gsartoretti/PRIMAL](https://github.com/gsartoretti/PRIMAL) | Classic RL+imitation-learning MAPF baseline. |
| PRIMAL2 | [marmotlab/PRIMAL2](https://github.com/marmotlab/PRIMAL2) | Lifelong extension of PRIMAL. |
| MAGAT | [proroklab/magat_pathplanning](https://github.com/proroklab/magat_pathplanning) | GNN-based MAPF approach with message-aware coordination. |
| HMAGAT | [proroklab/hmagat](https://github.com/proroklab/hmagat) | Hypergraph neural architecture for dense MAPF. |
| CTRM | [omron-sinicx/ctrm](https://github.com/omron-sinicx/ctrm) | Learns cooperative timed roadmaps for continuous-space MAPF. |
| SCRIMP | [marmotlab/SCRIMP](https://github.com/marmotlab/SCRIMP) | RL/IL approach emphasizing scalable inter-agent communication. |
| MAPF-GPT | [CognitiveAISystems/MAPF-GPT](https://github.com/CognitiveAISystems/MAPF-GPT) | Large-scale imitation-learning-based MAPF solver. |
| MAPF-GPT-DDG | [Cognitive-AI-Systems/MAPF-GPT-DDG](https://github.com/Cognitive-AI-Systems/MAPF-GPT-DDG) | MAPF-GPT variant with active fine-tuning. |



#### Hybrid
| Solver / Repository | Implementation | Description |
| --- | --- | --- |
| SSSP | [Kei18/sssp](https://github.com/Kei18/sssp) | Hybrid motion planner that combines search and sampling. |
| LNS2+RL | [marmotlab/LNS2-RL](https://github.com/marmotlab/LNS2-RL) | Hybrid approach combining LNS2 with learned policies. |
| Improving ML MAPF Policies with Heuristic Search | [Rishi-V/ML-MAPF-with-Search](https://github.com/Rishi-V/ML-MAPF-with-Search) | Focuses on improving the performance of learned single-stage policies in MAPF using heuristic search techniques |
| LaGAT | [proroklab/lagat](https://github.com/proroklab/lagat) | Combining neural policy heuristic methods with the enhanced MAGAT+ model |
| distill-lagat | [proroklab/distill-lagat](https://github.com/proroklab/distill-lagat/tree/main) | simplified version of LaGAT |


#### Others
| Solver / Repository | Implementation | Description |
| --- | --- | --- |
| Python PathPlanning algorithms | [zhm-real/PathPlanning](https://github.com/zhm-real/PathPlanning) | Python collection of multiple MAPF methods. |
| Python MAPF algorithms | [atb033/multi_agent_path_planning](https://github.com/atb033/multi_agent_path_planning) | Python collection of multiple MAPF methods. |
| Java MAPF algorithms | [J-morag/MAPF](https://github.com/J-morag/MAPF) | Java collection of multiple MAPF methods. |


### Benchmarks & Visualization Tools & Testbed
| Tool / Repository | Link | Description |
| --- | --- | --- |
| pogema | [Cognitive-AI-Systems/pogema](https://github.com/Cognitive-AI-Systems/pogema) | Grid-world environment and simulator widely used for MAPF learning and evaluation. |
| pogema-benchmark | [Cognitive-AI-Systems/pogema-benchmark](https://github.com/Cognitive-AI-Systems/pogema-benchmark) | Benchmark harness and evaluation setup for running standardized MAPF experiments. |
| pogema-toolbox | [Cognitive-AI-Systems/pogema-toolbox](https://github.com/Cognitive-AI-Systems/pogema-toolbox) | Utilities and helper tools for generating maps, scenarios, and experiment workflows around Pogema. |
| mapf-visualizer (Keisuke Okumura) | [kei18/mapf-visualizer](https://github.com/kei18/mapf-visualizer) | Lightweight visualizer for MAPF instance playback and solver result inspection. |
| SMART Simulator (organization) | [smart-mapf](https://github.com/smart-mapf) | Organization hosting simulator and ecosystem projects for realistic lifelong MAPF studies. |
| SMART Simulator Demo | [smart-mapf demo](https://smart-mapf.github.io/demo/) | Browser demo for quickly testing and viewing SMART simulator behavior. |
| LSMART | [smart-mapf/lifelong-smart](https://github.com/smart-mapf/lifelong-smart) | Lifelong Scalable Multi-Agent Realistic Testbed for long-horizon MAPF research. |

## Websites　&#x1f5a5;
- [mapf.info](https://mapf.info/)
- [Pathfinding Benchmarks](https://movingai.com/benchmarks/index.html)
- [Project "Multi-Agent Path Planning (MAPF)"](https://idm-lab.org/project-p.html)
- [A Project on Multi-Agent Path Finding](https://modelai.gettysburg.edu/2020/mapf/)
- [Foundations of Multi-Agent Path Finding](https://jiaoyangli.me/research/mapf/)
- [マルチエージェント経路計画の紹介](https://kei18.github.io/note/posts/mapf-tutorial/)


## Videos　&#x1f3a5;
- [Lecture 9: Multi-Robot Path Planning(2021)](https://www.youtube.com/watch?v=VJkFHIUHHXw)
- [AAMAS-22 Tutorial on Recent Advances in Multi-Agent Path Finding(2022)](https://www.youtube.com/watch?v=H3wRCZf_Mrs)
- [ICRA25: Multi-Agent Path Finding Using Conflict-Based Search and Structural-Semantic Topometric Maps(2025)](https://www.youtube.com/watch?v=j3UU694Ils0)
- [Upgrading Multi-Agent Pathfinding for the Real World(2026)](https://www.youtube.com/watch?v=XeZTyUS8ZF0)
- [Autonomy Talks - 奥村 圭介: スケーラブルなMAPFから高性能なマルチロボット協調まで(2026)](https://www.youtube.com/watch?v=xI84VltsVRw)

---

> References
> - [awesome-mapf](https://github.com/joonyeol-sim/awesome-mapf?tab=readme-ov-file) ```Reference list used for literature search```
> - [pogema](https://github.com/Cognitive-AI-Systems/pogema) ```Used for creating demos of assets```
