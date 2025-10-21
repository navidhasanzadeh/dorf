# DoRF: Doppler Radiance Fields for Robust Human Activity Recognition Using Wi-Fi

Navid Hasanzadeh, Shahrokh Valaee

Wireless and Internet Research Laboratory (WIRLab)

University of Toronto

## Introduction
Commodity Wi-Fi devices continuously monitor how their signals propagate through an environment, bouncing off walls, furniture, and people. From these echoes, they estimate the wireless channel—captured as Channel State Information (CSI)—between a transmitter and its receivers. When a person moves, the echoes shift, creating Doppler shifts that are directly related to motion velocity. Wi-Fi-based Human Activity Recognition (HAR) interprets these subtle variations to track motion without cameras or wearables, enabling non-intrusive and privacy-preserving sensing. However, most existing approaches struggle to generalize, often suffering from significant performance drops when evaluated on new users or unseen environments.

Our proposed method, Doppler Radiance Fields (DoRF), views motion as if it were captured by multiple cameras placed around the user—but in the Doppler domain rather than the visual domain. It extracts multiple Doppler velocity projections from Wi-Fi CSI, with each projection acting like a virtual one-dimensional camera that observes the motion from a different direction. Just as real cameras provide diverse viewpoints that help reconstruct a 3D scene, these Doppler projections offer complementary perspectives on how the hand moves through space. Inspired by Neural Radiance Fields (NeRF)—which rebuild full 3D structure from a set of 2D images—DoRF fuses its Doppler “views” to recover a latent 3D motion representation. This novel approach enables a comprehensive, robust, and view-invariant understanding of activity, overcoming the limitations of prior CSI-based methods and significantly improving generalization to unseen users and environments.
