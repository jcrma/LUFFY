# LUFFY Development Repository

> 🚧 **Development Branch** - This is the main development repository for LUFFY (Learning to Reason Under Off‑Policy Guidance)

## About LUFFY

LUFFY is a reinforcement learning framework that bridges the gap between zero-RL and imitation learning by incorporating off-policy reasoning traces into the training process. This repository contains the core implementation and development work.

## 🔧 Development Status

This repository is under active development. Many features are currently being implemented or need refactoring.

## 🚀 Quick Start

⚠️ **Note**: This development version has incomplete implementations. Many features are marked as TODO and need to be completed before production use.

```bash
# Clone the repository
git clone <repository-url>
cd LUFFY

# Install dependencies
pip install -r luffy/requirements.txt

# Note: Some functionality is incomplete - check TODO list below for details
```

## 📁 Repository Structure

```
LUFFY/
├── luffy/                 # Core framework
│   ├── deepscaler/        # Scaling utilities (⚠️ Gemini API integration still needed)
│   ├── verl/              # RL training components (⚠️ Some features incomplete)
│   └── ...
├── data/                  # Training data and scripts
├── eval_scripts/          # Evaluation utilities
├── exp_scripts/           # Experiment scripts
└── README.md              # This file
```

## ⚠️ Development Notes

- This is a **development version** with incomplete implementations
- Many functions contain TODO markers indicating pending work
- OpenAI API integration is implemented, but Gemini API integration is still a placeholder
- FSDP and distributed training features need completion


### 🔴 High Priority TODOs

- **API Integration**: Gemini API implementation still needs completion
- **Reward System**: Parallel processing and validation for reward computation  
- **FSDP Training**: Model loading and distributed training setup
- **Data Processing**: Batch dimension optimization TODOs remain

### 📝 Complete TODO List

- [ ] **luffy/deepscaler/utils.py:45** - TODO: Add logging for API calls and errors
- [ ] **luffy/deepscaler/utils.py:46** - TODO: Support batch processing for multiple prompts
- [ ] **luffy/deepscaler/utils.py:47** - TODO: Add timeout configuration for API calls
- [ ] **luffy/deepscaler/utils.py:107** - TODO: Implement Vertex AI initialization and authentication
- [ ] **luffy/deepscaler/utils.py:108** - TODO: Configure safety settings for content generation
- [ ] **luffy/deepscaler/utils.py:109** - TODO: Set up GenerativeModel with proper system instructions
- [ ] **luffy/deepscaler/utils.py:110** - TODO: Implement retry logic with exponential backoff
- [ ] **luffy/deepscaler/utils.py:111** - TODO: Add comprehensive error handling for API access issues
- [ ] **luffy/deepscaler/utils.py:112** - TODO: Handle rate limiting and quota management
- [ ] **luffy/deepscaler/utils.py:113** - TODO: Implement response validation and text extraction
- [ ] **luffy/deepscaler/utils.py:114** - TODO: Add support for different generation configurations
- [ ] **luffy/test.py:1590** - TODO: add smaller page sizes when https://github.com/Dao-AILab/flash-attention/pull/824 is merged
- [ ] **luffy/verl/examples/split_placement/split_monkey_patch.py:141** - TODO: make a canonical logger that supports various backend
- [ ] **luffy/verl/tests/e2e/check_results.py:21** - TODO: this function needs error handling
- [ ] **luffy/verl/tests/model/test_transformer.py:22** - TODO(sgm): add more models for test
- [ ] **luffy/verl/tests/model/test_transformer.py:50** - TODO(sgm): we can construct the position_ids_rmpad here
- [ ] **luffy/verl/tests/model/test_transformer.py:111** - TODO(sgm): we can construct the position_ids_rmpad here
- [ ] **luffy/verl/tests/model/test_transformers_ulysses.py:34** - TODO(sgm): add more models for test
- [ ] **luffy/verl/tests/model/test_transformers_ulysses.py:81** - TODO(sgm): we can construct the position_ids_rmpad here
- [ ] **luffy/verl/tests/model/test_transformers_ulysses.py:159** - TODO(sgm): we can construct the position_ids_rmpad here
- [ ] **luffy/verl/tests/ray/test_high_level_scheduling_api.py:25** - TODO: pass *args and **kwargs is bug prone and not very convincing
- [ ] **luffy/verl/tests/ray/test_worker_group_basics.py:43** - TODO: pass *args and **kwargs is bug prone and not very convincing
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:54** - TODO(sgm): support FSDP hybrid shard for larger model
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:83** - TODO: it seems that manual offload is slowly than FSDP offload
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:123** - TODO(zhangchi.usc1992): 1. support create from random initialized model. 2. Support init with FSDP directly
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:199** - TODO(zhangchi.usc1992, shengguangming) fix me. Current, auto_wrap_policy causes HFRollout to hang in Gemma
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:207** - TODO: add transformer policy
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:226** - TODO: add more optimizer args into config
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:252** - TODO(sgm): support FSDP hybrid shard for larger model
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:263** - TODO: a sharding manager that do nothing?
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:391** - TODO: here, we should return all metrics
- [ ] **luffy/verl/verl/mix_src/mix_fsdp_worker.py:517** - TODO: support DCP and save sharded checkpoints
- [ ] **luffy/verl/verl/mix_src/mix_trainer.py:90** - TODO: add other ways to estimate advantages
- [ ] **luffy/verl/verl/mix_src/mix_trainer.py:168** - TODO: support each role have individual ray_worker_group_cls,
- [ ] **luffy/verl/verl/mix_src/mix_trainer.py:293** - TODO: we have to make sure the batch size is divisible by the dp size
- [ ] **luffy/verl/verl/mix_src/mix_trainer.py:599** - TODO: make a canonical logger that supports various backend
- [ ] **luffy/verl/verl/mix_src/mix_trainer.py:637** - TODO: add response length
- [ ] **luffy/verl/verl/mix_src/mix_trainer_acc_rebatch.py:63** - TODO: we have to make sure the batch size is divisible by the dp size
- [ ] **luffy/verl/verl/mix_src/mix_trainer_acc_rebatch.py:437** - TODO: make a canonical logger that supports various backend
- [ ] **luffy/verl/verl/mix_src/mix_trainer_acc_rebatch.py:592** - TODO: check path
- [ ] **luffy/verl/verl/mix_src/mix_trainer_acc_rebatch.py:628** - TODO: from remote not implemented yet
- [ ] **luffy/verl/verl/mix_src/mix_vllm_rollout.py:43** - TODO
- [ ] **luffy/verl/verl/models/llama/megatron/layers/parallel_attention.py:380** - TODO: llama does not have dropout in the config??
- [ ] **luffy/verl/verl/models/llama/megatron/layers/parallel_decoder.py:78** - TODO: add sequence parallel operator reduce_scatter here
- [ ] **luffy/verl/verl/models/llama/megatron/layers/parallel_decoder.py:86** - TODO: add sequence parallel operator all_gather here
- [ ] **luffy/verl/verl/models/llama/megatron/layers/parallel_decoder.py:90** - TODO: add sequence parallel operator reduce_scatter here
- [ ] **luffy/verl/verl/models/llama/megatron/modeling_llama_megatron.py:330** - TODO: for better performance, the sp padding should be removed at each layer. Not sure the performance gap
- [ ] **luffy/verl/verl/models/llama/megatron/modeling_llama_megatron.py:588** - TODO: for better performance, the sp padding should be removed at each layer. Not sure the performance gap
- [ ] **luffy/verl/verl/models/registry.py:21** - TODO(sgm): HF may supported more than listed here, we should add more after testing
- [ ] **luffy/verl/verl/models/transformers/llama.py:88** - TODO: These transpose are quite inefficient but Flash Attention requires the layout [batch_size, sequence_length, num_heads, head_dim]. We would need to refactor the KV cache
- [ ] **luffy/verl/verl/protocol.py:114** - TODO: Optimize memory usage during tensor reshaping
- [ ] **luffy/verl/verl/protocol.py:115** - TODO: Add support for different tensor types and shapes
- [ ] **luffy/verl/verl/protocol.py:136** - TODO: Optimize tensor view operations for performance
- [ ] **luffy/verl/verl/protocol.py:137** - TODO: Add error handling for invalid batch dimensions
- [ ] **luffy/verl/verl/protocol.py:169** - TODO(zhangchi.usc1992) add consistency check
- [ ] **luffy/verl/verl/protocol.py:265** - TODO: we can actually lift this restriction if needed
- [ ] **luffy/verl/verl/protocol.py:351** - TODO (zhangchi.usc1992) whether to copy
- [ ] **luffy/verl/verl/single_controller/ray/base.py:439** - TODO: create a class with customizable name
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/arg_utils.py:64** - TODO(shengguangming): delete the unused args
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/arg_utils.py:147** - TODO(woosuk): Support fine-grained seeds (e.g., seed per request).
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/llm.py:237** - TODO(shengguangming): maybe we can hack the autoregressive logics without only apply post process for better performance
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/llm.py:241** - TODO(sgm): we can optimize it by making the dataloader yield List[int] without padding.
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/llm.py:257** - TODO(shengguangming): can be optimzied by rewrite the Sampler._get_logprobs() logits
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/llm_engine_sp.py:99** - TODO(woosuk): Print more configs in debug mode.
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/llm_engine_sp.py:101** - TODO: currently is hfconfig
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/llm_engine_sp.py:112** - TODO(shengguangming): maybe we can choose init here or from arguments
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/llm_engine_sp.py:145** - TODO: check get_lora_tokenizer func
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/llm_engine_sp.py:586** - TODO: check this input
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/llm_engine_sp.py:661** - TODO: we may not need to decode
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/model_loader.py:67** - TODO(shengguangming): latest commit in vllm fix awq for this function and add load_weights
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/model_loader.py:96** - TODO (pad to be divided by 4)
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/model_loader.py:224** - TODO(zhuohan): Change the get_logits part to a separate stage.
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/tokenizer.py:56** - TODO(sgm): the lora tokenizer is also passed, but may be different
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/weight_loaders.py:62** - TODO: check megatron
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/weight_loaders.py:84** - TODO: need to implement a general way to deal with prefix
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/worker.py:109** - TODO: do not use cupy
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/worker.py:209** - TODO(woosuk): Profile swapping overhead and optimize if needed.
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_3_1/worker.py:291** - TODO (shengguangming): maybe we should also flag the megatron is initialized
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/arg_utils.py:44** - TODO
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/arg_utils.py:109** - TODO(shengguangming): delete the unused args
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/arg_utils.py:192** - TODO(woosuk): Support fine-grained seeds (e.g., seed per request).
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/arg_utils.py:257** - TODO: spec config
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/config.py:136** - TODO: for multimodal model
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/hf_weight_loader.py:81** - TODO
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/llm.py:268** - TODO(shengguangming): maybe we can hack the autoregressive logics without only apply post process for better performance
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/llm.py:272** - TODO(sgm): we can optimize it by making the dataloader yield List[int] without padding.
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/llm.py:288** - TODO(shengguangming): can be optimzied by rewrite the Sampler._get_logprobs() logits
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/llm_engine_sp.py:128** - TODO(woosuk): Print more configs in debug mode.
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/llm_engine_sp.py:130** - TODO: currently is hfconfig
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/llm_engine_sp.py:143** - TODO(shengguangming): maybe we can choose init here or from arguments
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/llm_engine_sp.py:145** - TODO: check tokenizer class
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/llm_engine_sp.py:153** - TODO: don't know what's the usage
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/llm_engine_sp.py:228** - TODO(sgm): add for verl but we may not tokenizer in Rollout
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/llm_engine_sp.py:237** - TODO: check whether we should rebuild the CUDAGraph every iter when offload/load KVCache
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/megatron_weight_loaders.py:67** - TODO: check megatron
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/megatron_weight_loaders.py:254** - TODO: need to implement a general way to deal with prefix
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/megatron_weight_loaders.py:272** - TODO(shengguangming): latest commit in vllm fix awq for this function and add load_weights
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/megatron_weight_loaders.py:325** - TODO (pad to be divided by 4)
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/megatron_weight_loaders.py:337** - TODO: remove dependencies from megatron
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/model_loader.py:141** - TODO(sgm): This is a hack, we need to register the load_weight() func for each model in vllm
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/model_loader.py:226** - TODO(sgm): This is a hack, we need to register the load_weight() func for each model in vllm
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/model_runner.py:274** - TODO(sgm): perform sampling on rank 0
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/parallel_state.py:236** - TODO: this will hang
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/parallel_state.py:245** - TODO: will hang when used with device mesh
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/parallel_state.py:247** - TODO: init using device mesh
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/spmd_gpu_executor.py:62** - TODO(sgm): verl not support speculative decode now
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/spmd_gpu_executor.py:208** - TODO(sgm): not implemented async executor yet
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/tokenizer.py:61** - TODO(sgm): the lora tokenizer is also passed, but may be different
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/worker.py:30** - TODO(sgm): check why vllm has similar file in vllm.model_executor.parallel_utils.parallel_state
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_4_2/worker.py:270** - TODO(sgm): check whether need this
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/arg_utils.py:53** - TODO(sgm): check this
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/arg_utils.py:54** - TODO(sgm): check this
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/arg_utils.py:143** - TODO(shengguangming): delete the unused args
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/arg_utils.py:226** - TODO(woosuk): Support fine-grained seeds (e.g., seed per request).
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/arg_utils.py:366** - TODO: spec config
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/config.py:191** - TODO: check whether this is necessary
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/hf_weight_loader.py:32** - TODO
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/llm.py:148** - TODO: check usagecontext
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/llm.py:205** - TODO(sgm): we can optimize it by making the dataloader yield List[int] without padding.
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/llm.py:221** - TODO(shengguangming): can be optimzied by rewrite the Sampler._get_logprobs() logits
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/llm_engine_sp.py:143** - TODO(woosuk): Print more configs in debug mode.
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/llm_engine_sp.py:160** - TODO(shengguangming): maybe we can choose init here or from arguments
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/llm_engine_sp.py:262** - TODO(sgm): add for verl but we may not tokenizer in Rollout
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/llm_engine_sp.py:271** - TODO: check whether we should rebuild the CUDAGraph every iter when offload/load KVCache
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/megatron_weight_loaders.py:67** - TODO: check megatron
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/megatron_weight_loaders.py:254** - TODO: need to implement a general way to deal with prefix
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/megatron_weight_loaders.py:272** - TODO(shengguangming): latest commit in vllm fix awq for this function and add load_weights
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/model_loader.py:152** - TODO(sgm): This is a hack, we need to register the load_weight() func for each model in vllm
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/model_loader.py:239** - TODO(sgm): This is a hack, we need to register the load_weight() func for each model in vllm
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/parallel_state.py:94** - TODO(sgm): deviate from the v0.5.4, not pp now
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/parallel_state.py:138** - TODO: check why True is not work in Ray trainer
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/parallel_state.py:165** - TODO: check why True is not work in Ray trainer
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/parallel_state.py:177** - TODO: init using device mesh (not support hybrid engine now)
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/spmd_gpu_executor.py:66** - TODO(sgm): verl not support speculative decode now
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/spmd_gpu_executor.py:214** - TODO(sgm): not implemented async executor yet
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/tokenizer.py:66** - TODO(sgm): the lora tokenizer is also passed, but may be different
- [ ] **luffy/verl/verl/third_party/vllm/vllm_v_0_5_4/worker.py:34** - TODO(sgm): check why there is a similar file in vllm
- [ ] **luffy/verl/verl/trainer/ppo/ray_trainer.py:129** - TODO: add other ways to estimate advantages
- [ ] **luffy/verl/verl/trainer/ppo/ray_trainer.py:207** - TODO: add response length
- [ ] **luffy/verl/verl/trainer/ppo/ray_trainer.py:330** - TODO: support each role have individual ray_worker_group_cls,
- [ ] **luffy/verl/verl/trainer/ppo/ray_trainer.py:379** - TODO: we have to make sure the batch size is divisible by the dp size
- [ ] **luffy/verl/verl/trainer/ppo/ray_trainer.py:632** - TODO: check path
- [ ] **luffy/verl/verl/trainer/ppo/ray_trainer.py:667** - TODO: from remote not implemented yet
- [ ] **luffy/verl/verl/trainer/ppo/ray_trainer.py:880** - TODO: make a canonical logger that supports various backend
- [ ] **luffy/verl/verl/utils/checkpoint/fsdp_checkpoint_manager.py:101** - TODO: shall we remove previous ckpt every save?
- [ ] **luffy/verl/verl/utils/checkpoint/fsdp_checkpoint_manager.py:135** - TODO: address optimizer is None
- [ ] **luffy/verl/verl/utils/hdfs_io.py:67** - TODO(haibin.lin):
- [ ] **luffy/verl/verl/utils/hdfs_io.py:102** - TODO(haibin.lin):
- [ ] **luffy/verl/verl/utils/megatron_utils.py:202** - TODO(sgm): check how to disable megatron timers
- [ ] **luffy/verl/verl/utils/model.py:164** - TODO: we can make this faster
- [ ] **luffy/verl/verl/utils/model.py:272** - TODO: to find a better way to load mistral7b-rm lm_head
- [ ] **luffy/verl/verl/utils/torch_functional.py:362** - TODO: add them back
- [ ] **luffy/verl/verl/workers/actor/megatron_actor.py:158** - TODO (zhangchi.usc1992): actually, this function should only return log_prob and this logic should be handled by user outside
- [ ] **luffy/verl/verl/workers/actor/megatron_actor.py:225** - TODO: actually, we just need to control the sampling order.
- [ ] **luffy/verl/verl/workers/actor/megatron_actor.py:301** - TODO: we may use the new schedule instead
- [ ] **luffy/verl/verl/workers/critic/megatron_critic.py:176** - TODO: we may use the new schedule instead
- [ ] **luffy/verl/verl/workers/fsdp_workers.py:88** - TODO(sgm): support FSDP hybrid shard for larger model
- [ ] **luffy/verl/verl/workers/fsdp_workers.py:117** - TODO: it seems that manual offload is slowly than FSDP offload
- [ ] **luffy/verl/verl/workers/fsdp_workers.py:157** - TODO(zhangchi.usc1992): 1. support create from random initialized model. 2. Support init with FSDP directly
- [ ] **luffy/verl/verl/workers/fsdp_workers.py:225** - TODO(zhangchi.usc1992, shengguangming) fix me. Current, auto_wrap_policy causes HFRollout to hang in Gemma
- [ ] **luffy/verl/verl/workers/fsdp_workers.py:233** - TODO: add transformer policy
- [ ] **luffy/verl/verl/workers/fsdp_workers.py:252** - TODO: add more optimizer args into config
- [ ] **luffy/verl/verl/workers/fsdp_workers.py:278** - TODO(sgm): support FSDP hybrid shard for larger model
- [ ] **luffy/verl/verl/workers/fsdp_workers.py:289** - TODO: a sharding manager that do nothing?
- [ ] **luffy/verl/verl/workers/fsdp_workers.py:416** - TODO: here, we should return all metrics
- [ ] **luffy/verl/verl/workers/fsdp_workers.py:811** - TODO(sgm): we may need to extract it to dp_reward_model.py
- [ ] **luffy/verl/verl/workers/megatron_workers.py:106** - TODO(sgm): Currently, we only support reference model param offload
- [ ] **luffy/verl/verl/workers/megatron_workers.py:204** - TODO: add more optimizer args into config
- [ ] **luffy/verl/verl/workers/megatron_workers.py:338** - TODO: here, we should return all metrics
- [ ] **luffy/verl/verl/workers/megatron_workers.py:444** - TODO(sgm): support critic model offload
- [ ] **luffy/verl/verl/workers/megatron_workers.py:478** - TODO: support vpp here
- [ ] **luffy/verl/verl/workers/megatron_workers.py:507** - TODO: add more optimizer args into config
- [ ] **luffy/verl/verl/workers/megatron_workers.py:667** - TODO: add more optimizer args into config
- [ ] **luffy/verl/verl/workers/megatron_workers.py:720** - TODO: reward model use itself tokenizer instead of sft tokenizer
- [ ] **luffy/verl/verl/workers/reward_model/megatron/reward_model.py:145** - TODO(sgm): check why is bfloat16
- [ ] **luffy/verl/verl/workers/reward_model/megatron/reward_model.py:192** - TODO: actually, we just need to control the sampling order.
- [ ] **luffy/verl/verl/workers/reward_model/megatron/reward_model.py:233** - TODO: we may use the new schedule instead
- [ ] **luffy/verl/verl/workers/rollout/hf_rollout.py:98** - TODO: filter out the seq with no answers like ds-chat
- [ ] **luffy/verl/verl/workers/rollout/vllm_rollout/vllm_rollout.py:43** - TODO
- [ ] **luffy/verl/verl/workers/sharding_manager/fsdp_ulysses.py:49** - TODO: check how to set seed for each model
- [ ] **luffy/verl/verl/workers/sharding_manager/fsdp_ulysses.py:56** - TODO: check how to set seed for each model
- [ ] **luffy/verl/verl/workers/sharding_manager/fsdp_vllm.py:82** - TODO: offload FSDP model weights
- [ ] **luffy/verl/verl/workers/sharding_manager/fsdp_vllm.py:113** - TODO: Current impl doesn't consider FSDP with torch micro-dp
- [ ] **luffy/verl/verl/workers/sharding_manager/fsdp_vllm.py:122** - TODO: Current impl doesn't consider FSDP with torch micro-dp
- [ ] **luffy/verl/verl/workers/sharding_manager/fsdp_vllm.py:130** - TODO: shall we build a micro_dp group for vllm when integrating with vLLM?
- [ ] **luffy/verl/verl/workers/sharding_manager/megatron_vllm.py:76** - TODO: after binding to the memory buffer, we can load the checkpoint here
- [ ] **luffy/verl/verl/workers/sharding_manager/megatron_vllm.py:253** - TODO(sgm): this may not be true for FSDP -> vLLM
- [ ] **luffy/verl/verl/workers/sharding_manager/megatron_vllm.py:323** - TODO(zhangchi.usc1992) We can consider copy non-tp weight to another infer buffer.
