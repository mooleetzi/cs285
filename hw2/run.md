```bash
# experiments1 
python cs285/scripts/run_hw2.py --env_name CartPole-v0 -n 100 -b 1000 \
    -dsa --exp_name q1_sb_no_rtg_dsa --which_gpu "1"
python cs285/scripts/run_hw2.py --env_name CartPole-v0 -n 100 -b 1000 \
    -rtg -dsa --exp_name q1_sb_rtg_dsa --which_gpu "1"
python cs285/scripts/run_hw2.py --env_name CartPole-v0 -n 100 -b 1000 \
    -rtg --exp_name q1_sb_rtg_na --which_gpu "1"
python cs285/scripts/run_hw2.py --env_name CartPole-v0 -n 100 -b 5000 \
    -dsa --exp_name q1_lb_no_rtg_dsa --which_gpu "1"
python cs285/scripts/run_hw2.py --env_name CartPole-v0 -n 100 -b 5000 \
    -rtg -dsa --exp_name q1_lb_rtg_dsa --which_gpu "1"
python cs285/scripts/run_hw2.py --env_name CartPole-v0 -n 100 -b 5000 \
    -rtg --exp_name q1_lb_rtg_na --which_gpu "1"


# experiments2
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b <b*> -lr <r*> -rtg \
    --exp_name q2_b<b*>_r<r*> --which_gpu "1"
# first try, b=1000, lr=0.005 -> max return 1000 
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 1000 -lr 0.005 -rtg \
    --exp_name q2_b1000_r0.005 --which_gpu "1"

# second try, b=1000, lr=0.005 -> max return 1000
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 800 -lr 0.005 -rtg \
    --exp_name q2_b800_r0.005 --which_gpu "1"

# third try, b=600, lr=0.005 -> max return 1000
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 600 -lr 0.005 -rtg \
    --exp_name q2_b600_r0.005 --which_gpu "1"

# fourth try, b=400, lr=0.005 -> max return 1000
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 400 -lr 0.005 -rtg \
    --exp_name q2_b400_r0.005 --which_gpu "1"

# fifth try, b=200, lr=0.005 -> max return 323
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 200 -lr 0.005 -rtg \
    --exp_name q2_b200_r0.005 --which_gpu "1"

# sixth try, b=300, lr=0.005 -> max return 860
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 300 -lr 0.005 -rtg \
    --exp_name q2_b300_r0.005 --which_gpu "1"

# seventh try, b=350, lr=0.005 -> max return 1000
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 350 -lr 0.005 -rtg \
    --exp_name q2_b350_r0.005 --which_gpu "1"

# eighth try, b=350, lr=0.01 -> max return 260
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 350 -lr 0.01 -rtg \
    --exp_name q2_b350_r0.01 --which_gpu "1"

# ninth try, b=350, lr=0.007 -> max return 1000
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 350 -lr 0.007 -rtg \
    --exp_name q2_b350_r0.007 --which_gpu "1"

# tenth try, b=350, lr=0.008 -> max return 1000
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 350 -lr 0.008 -rtg \
    --exp_name q2_b350_r0.008 --which_gpu "1"

# eleventh try, b=350, lr=0.009 -> max return 1000
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 350 -lr 0.009 -rtg \
    --exp_name q2_b350_r0.009 --which_gpu "1"

# twelfth try, b=350, lr=0.0095 -> max return 640
python cs285/scripts/run_hw2.py --env_name InvertedPendulum-v2 \
    --ep_len 1000 --discount 0.9 -n 100 -l 2 -s 64 -b 350 -lr 0.0095 -rtg \
    --exp_name q2_b350_r0.0095 --which_gpu "1"


# experiments3
python cs285/scripts/run_hw2.py \
    --env_name LunarLanderContinuous-v2 --ep_len 1000 \
    --discount 0.99 -n 100 -l 2 -s 64 -b 40000 -lr 0.005 \
    --reward_to_go --nn_baseline --exp_name q3_b40000_r0.005 --which_gpu "1"

```