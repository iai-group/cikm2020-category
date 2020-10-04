# Generating Categories for Sets of Entities


This repository contains resources developed within the following paper:

> S. Zhang, K. Balog and J. Callan. Generating Categories for Sets of Entities. In: *Proceedings of the 29th ACM International Conference on Information and Knowledge Management*, Oct 2020. 

## Benchmark

* `category_generation/training_data_for_candidate_generation` stores the training, validation, and test data for candidate generation in JSON format. The number of training, validation, and test data is 8432, 1055, and 1055 respectively. Any instance with id ``table-xxxx-xxxx`` corresponds to a Wikipedia table or list, where an entity set is embedded. We take these entities' categories, which having over half of the entities in the set as members, as ground truth categories. These categories are futher parsed, see `category_generation/candidate_categories/sqs_all.*`

* The feature files for ranking the categories in test data are located in `feature_file_for_training_instances`.

  
## Citation
```
@inproceedings{Zhang:2020:GCS,
	author = {Zhang, Shuo and Balog, Krisztian and Callan, Jamie},
	title = {Generating Categories for Sets of Entities},
	year = {2020},
	booktitle = {Proceedings of the 29th ACM International Conference on Information and Knowledge Management},
	series = {CIKM '20}
}
```

## Contact
If you have any questions, please contact Shuo Zhang at imsure318@gmail.com.
