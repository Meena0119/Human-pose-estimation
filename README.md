#human-pose-estimation:
Use Case and High-Level Description:-
This is a multi-person 2D pose estimation network (based on the OpenPose approach) with tuned MobileNet v1 as a feature extractor. For every person in an image, the network detects a human pose: a body skeleton consisting of keypoints and connections between them. The pose may contain up to 18 keypoints: ears, eyes, nose, neck, shoulders, elbows, wrists, hips, knees, and ankles.
Inputs:-
Image, name: data, shape: 1, 3, 256, 456 in the B, C, H, W format, where:
B - batch size
C - number of channels
H - image height
W - image width
Install dependencies:-
pip install -r requirements.txt
Make libs:-
cd ${POSE_ROOT}/lib
make

Init output(training model output directory) and log(tensorboard log directory) directory:-

mkdir output 
mkdir log

Your directory tree should look like this:=

${POSE_ROOT}
├── data
├── experiments
├── lib
├── log
├── models
├── output
├── pose_estimation
├── README.md
└── requirements.txt



