# Generating Categories for Sets of Entities


This repository contains resources developed within the following paper:

> S. Zhang, K. Balog and J. Callan. Generating Categories for Sets of Entities. In: *Proceedings of the 29th ACM International Conference on Information and Knowledge Management*, Oct 2020. 

## Benchmark

### Candidate Generation

* `category_generation/training_data_for_candidate_generation` stores the training, validation, and test data for candidate generation in JSON format. The number of training, validation, and test data is 8432, 1055, and 1055 respectively. Any instance with id ``table-xxxx-xxxx`` corresponds to a Wikipedia table or list, where an entity set is embedded. We take these entities' categories, which having over half of the entities in the set as members, as ground truth categories. These categories are futher parsed, see `category_generation/candidate_categories/sqs_all.*`

* The feature files for initial ranking the categories in test data are located in `feature_file_for_training_instances`

* `feature_file_for_training_instances/training_parent.csv`: <candidate category, parent categories, rel> for 1055 test data

### Parent Category Identification

* `cate_token_mapping.json.zip`: the graph model

* `run_files`: all the run files for this task

* `gt_files/query_cat.tsv`: 5000 Wikepedia child categories

* `gt_files/qrels_cat.tsv`: ground truth parent categories

### Final Ranking

* `training_new.csv`: training categories for final ranking, which consists of 5K positive cases (exists in 2012, 2016, and 2019) and 5K negative cases (existed in 2012, then deleted or replaced)

* `final_ranking/c_imp.json`: importance features for both training (`training_new.csv`)

* `final_ranking/yiwan.json`: structure and content features for both training (`training_new.csv`)

Training & Validation data and features:
<training_new.csv, yiwan.json, c_imp.json>

Test data and features:
<sqs_all.csv, sqs_feat_all.json, c_imp_sqs.json>

  
## Citation
```
@inproceedings{Zhang:2020:GCS,
	author = {Zhang, Shuo and Balog, Krisztian and Callan, Jamie},
	title = {Generating Categories for Sets of Entities},
	year = {2020},
	booktitle = {Proceedings of the 29th ACM International Conference on Information and Knowledge Management},
	series = {CIKM '20},
	pages = {1833–1842}
}
```

## Contact
If you have any questions, please contact Shuo Zhang at imsure318@gmail.com.
