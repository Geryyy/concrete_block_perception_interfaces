# concrete_block_perception_interfaces

ROS 2 interfaces for the perception providers in the concrete-block stack — short-lived per-frame detections and the ICP registration action server. Companion to [concrete_block_perception](../concrete_block_perception/) (which implements the providers) and [concrete_block_world_model](../concrete_block_world_model/) (which consumes them).

## Contents

| Kind | Name | Used by |
|---|---|---|
| `msg` | `TrackedDetection`, `TrackedDetectionArray` | `block_detection_tracking_node` → `world_model_node` |
| `srv` | `TrackDetections` | per-frame detection tracker call |
| `srv` | `SegmentAtPoint` | on-demand YOLO segmentation at a 2D point |
| `srv` | `RegisterBlock` | single-shot ICP registration |
| `action` | `RegisterBlock` | long-running ICP registration with progress feedback |

For the *persistent* block-state / planning-scene API used by motion planning and the BT, see [concrete_block_world_model_interfaces](../concrete_block_world_model_interfaces/).

## Build

```bash
colcon build --packages-select concrete_block_perception_interfaces
```
