behavior cloning:
```bash
    python cs285/scripts/run_hw1.py --expert_policy_file cs285/policies/experts/Ant.pkl --env_name Ant-v2 --exp_name bc_ant --n_iter 1 --expert_data cs285/expert_data/expert_data_Ant-v2.pkl --video_log_freq -1  --which_gpu "1" 
```

DAgger:
```bash
    python cs285/scripts/run_hw1.py --expert_policy_file cs285/policies/experts/Ant.pkl --env_name Ant-v2 --exp_name dagger_ant --n_iter 10  --do_dagger --expert_data cs285/expert_data/expert_data_Ant-v2.pkl --video_log_freq -1  --which_gpu "1" 
    python cs285/scripts/run_hw1.py --expert_policy_file cs285/policies/experts/Humanoid.pkl --env_name Humanoid-v2 --exp_name dagger_humanoid --n_iter 10  --do_dagger --expert_data cs285/expert_data/expert_data_Humanoid-v2.pkl --video_log_freq -1  --which_gpu "1" 
```
