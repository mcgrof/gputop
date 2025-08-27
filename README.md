# gputop

I got tired of being told to use different tools to monitor one vendor
GPU or inference device against another so this is my effort to provide
a unified front to this in a way I think makse sense:

  * json collection while we use console monitoring
  * final png collection
  * multi-GPU / accelerator device

## Example Run

The `images/` directory contains example output from a test run monitoring ResNet-18 training using [AdamWPrune](https://github.com/mcgrof/AdamWPrune) on an AMD Radeon Pro W7900:

- **Performance Plot**: [`stats-amd-20250827-014218_plot.png`](images/stats-amd-20250827-014218_plot.png) - Visual graphs showing GPU utilization, memory usage, temperature, and power consumption over time
- **Summary Report**: [`stats-amd-20250827-014218_summary.txt`](images/stats-amd-20250827-014218_summary.txt) - Text summary with average, min, and max statistics

### Test Results Summary
- **Duration**: 41 minutes (2471 seconds) of ResNet-18 training
- **GPU Utilization**: 63.6% average (100% peak)
- **Memory Usage**: 1.7% average (2.6% peak) 
- **Temperature**: Edge 56.3°C avg, Junction 72.7°C avg, Memory 69.1°C avg
- **Power Draw**: 164.6W average (249W peak)
