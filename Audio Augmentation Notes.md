# Audio Augmentation Notes - DAP 1070/1071

### Audio_augmentation/testing CLI Run Command
```python main.py --test-data-csv-file=gs://dap_audio_augmentation_testing_dev/test_data/test.csv --env=dev --sample-rate=1600 --target-audio-length=15 --runner=dataflow```

### Required params:
    --test-data-csv-file=gs://dap_audio_augmentation_testing_dev/test_data/test.csv 
    --env=dev 
    --sample-rate=1600
    --target-audio-length=15
    --runner=dataflow


### Audio_augmentation/training CLI Run Command:
    ?
### Required params:
    --annotation-project-id
    --version
    --sample-rate
    --target-audio-length
    --target-audio-type
    --env
    --runner


## Task: Migrate audio augmentation data from old project (datascience-181217) to new project (data-science-platform-dev)

### Step 1: Transfer testing data from old bucket to new 
#### Testing Data Source
Project: ```data-science-platform-dev``` <br>
Bucket Name: ```dap_audio_augmentation_testing_dev``` <br>
Link: https://console.cloud.google.com/storage/browser/dap_audio_augmentation_testing_dev;tab=objects?forceOnBucketsSortingFiltering=false&project=data-science-platform-dev&prefix=&forceOnObjectsSortingFiltering=false <br>
#### Testing Data Destination 
Project: ```data-science-platform-dev``` <br>
Bucket Name: ```dap-audio-aug-test-dev```<br>
Link: https://console.cloud.google.com/storage/browser/dap-audio-aug-test-dev;tab=objects?forceOnBucketsSortingFiltering=false&project=data-science-platform-dev&prefix=&forceOnObjectsSortingFiltering=false <br>
dev update to  output bucket dap_audio_augmentation_testing and service account dap-audio-augmentation
### Step 2: Transfer training data from old bucket to new
#### Training Data Source
Project: ```datascience-181217``` <br>
Bucket Name: ```dap_audio_augmentation_dev``` <br>
Link: https://console.cloud.google.com/storage/browser/dap_audio_augmentation_dev;tab=objects?forceOnBucketsSortingFiltering=false&project=datascience-181217&prefix=&forceOnObjectsSortingFiltering=false <br>
#### Training Data Destination
Project: ```datascience-181217``` <br>
Bucket Name: ```dap-audio-aug-train-dev```<br>
Link: https://console.cloud.google.com/storage/browser/dap-audio-aug-train-dev;tab=objects?forceOnBucketsSortingFiltering=false&project=data-science-platform-dev&prefix=&forceOnObjectsSortingFiltering=false <br>

config.py requires update to output bucket dap_audio_augmentation_training and service account dap-audio-augmentation. <br>

Config file seems to have been moved already. 