sqs_feat_all.json (feature file for sqs_all.csv): c_is_e, lc_is_e, c_len_sw, has_p, has_sw, ctn_max, ctn_min, ctn_sum, ctn_avg, cec_max, cec_min, cec_sum, cec_avg+scores + scores_e + scores_cdbm25 + scores_cdbm25_soft + scores_ccbm25 + scores_ccbm25_soft+scores_body+scores_body_skos -- instance_neg_final.py

c_imp_sqs.json (importance feature file for sqs_all.csv): stat = [max(ttt), min(ttt), sum(ttt), sum(ttt)/len(ttt)] + [max(tmp_in), min(tmp_in), sum(tmp_in), sum(tmp_in)/len(tmp_in)] if len(tmp_in)>0 else [0]*4 + [int(outs.get(en, 0)) for en in ens] + [max(tmp_out), min(tmp_out), sum(tmp_out), sum(tmp_out)/len(tmp_out)] if len(tmp_out)>0 else [0]*4 -- c_graph_final.py

yiwan.json (feature file for training_parent.csv): c_is_e, lc_is_e, c_len_sw, has_p, has_sw, ctn_max, ctn_min, ctn_sum, ctn_avg, cec_max, cec_min, cec_sum, cec_avg+scores + scores_e + scores_cdbm25 + scores_cdbm25_soft + scores_ccbm25 + scores_ccbm25_soft+scores_body+scores_body_skos -- negative_final.json

c_imp (feature file for training_parent.csv): as above -- c_graph_final.py