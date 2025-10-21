# DoRF: Doppler Radiance Fields for Robust Human Activity Recognition Using Wi-Fi

Navid Hasanzadeh, Shahrokh Valaee


[Project website](https://navidhasanzadeh.github.io/dorf/)

[arXiv:2509.15129](https://arxiv.org/abs/2509.15129) (Our Latest work - _Generalization accuracy increased to 65.3%_)

[arXiv:2308.02425](https://arxiv.org/abs/2507.12132) (DoRF Original Paper)

[UTHAMO dataset](https://ieee-dataport.org/documents/uthamo-multi-modal-wi-fi-csi-based-hand-motion-dataset-0)


The paper has been accepted by IEEE International Workshop on Computational Advances in Multi-Sensor Adaptive Processing (IEEE CAMSAP 2025).

## Introduction
Commodity Wi-Fi devices continuously monitor how their signals propagate through an environment, bouncing off walls, furniture, and people. From these echoes, they estimate the wireless channel—captured as Channel State Information (CSI)—between a transmitter and its receivers. When a person moves, the echoes shift, creating Doppler shifts that are directly related to motion velocity. Wi-Fi-based Human Activity Recognition (HAR) interprets these subtle variations to track motion without cameras or wearables, enabling non-intrusive and privacy-preserving sensing. However, most existing approaches struggle to generalize, often suffering from significant performance drops when evaluated on new users or unseen environments.

Our proposed method, Doppler Radiance Fields (DoRF), views motion as if it were captured by multiple cameras placed around the user—but in the Doppler domain rather than the visual domain. It extracts multiple Doppler velocity projections from Wi-Fi CSI, with each projection acting like a virtual one-dimensional camera that observes the motion from a different direction. Just as real cameras provide diverse viewpoints that help reconstruct a 3D scene, these Doppler projections offer complementary perspectives on how the hand moves through space. Inspired by Neural Radiance Fields (NeRF)—which rebuild full 3D structure from a set of 2D images—DoRF fuses its Doppler “views” to recover a latent 3D motion representation. This novel approach enables a comprehensive, robust, and view-invariant understanding of activity, overcoming the limitations of prior CSI-based methods and significantly improving generalization to unseen users and environments.

## Dataset

UTHAMO is a multi-modal dataset developed for Wi-Fi-based human activity recognition (HAR), focusing on hand motion classification and generalization. The dataset contains Channel State Information (CSI) recordings of four right-hand gestures—Circle, Left-right, Up-Down, and Push-Pull—performed by six adult participants in a controlled indoor environment. Gestures were recorded across four body orientations (0°, 45°, 90°, and 180°) using five ASUS RT-AC86U access points, each with three antennas operating in passive monitor mode at 100 Hz in the 2.4GHz band. A Raspberry Pi served as the transmitter. Each gesture sample consists of five seconds of CSI data, collected over 20 trials per gesture–orientation pair, resulting in a total of 1,920 labeled samples. CSI was extracted using the Nexmon toolkit, yielding complex-valued matrices of size 3x64x500 per AP. To enable multi-modal verification and cross-modal learning, the dataset also includes synchronized video recordings from six perspectives—five cameras positioned behind each access point and one user-facing camera—as well as motion data from an inertial measurement unit (IMU) worn on the user’s wrist. The IMU captures accelerometer, gyroscope, and magnetometer signals during gesture execution. The gesture set was designed to exhibit similar two-dimensional projections in different planes, making them difficult to distinguish when the observer’s viewpoint is unknown. This configuration creates a challenging benchmark for evaluating the robustness and generalization performance of HAR models under varying perspectives and sensing modalities.

Please cite as:

```bibtex
@article{hasanzadeh2025dorf,
  title={DoRF: Doppler radiance fields for robust human activity recognition using Wi-Fi},
  author={Hasanzadeh, Navid and Valaee, Shahrokh},
  journal={arXiv preprint arXiv:2507.12132},
  year={2025}
}
```
