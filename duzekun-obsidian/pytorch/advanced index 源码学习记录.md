/MLU_OPS/DEV_SOFT_TRAIN/duzekun/pytorch_1.13/pytorch/aten/src/ATen/native/cuda/IndexKernel.cu
line53 gpu 实现

/MLU_OPS/DEV_SOFT_TRAIN/duzekun/pytorch_1.13/pytorch/aten/src/ATen/native/TensorAdvancedIndexing.cpp

line 2236 有可能是 bool tensor to long tensor 的转换。
line 548 AdvancedIndex::AdvancedIndex(const Tensor& src, TensorList indices_list)

/MLU_OPS/DEV_SOFT_TRAIN/duzekun/pytorch_1.13/pytorch/aten/src/ATen/native/TensorAdvancedIndexingUtils.h

line 58 static AdvancedIndex make_info(Tensor self, IOptTensorListRef orig) 内 return AdvancedIndex(self, indices) 

checkIndexTensorTypes

// first expand BoolTensor (masks) or ByteTensor (masks) into 1 or more LongTensors
auto indices = expandTensors(self, orig);

/MLU_OPS/DEV_SOFT_TRAIN/duzekun/pytorch_1.13/pytorch/aten/src/ATen/native/IndexingUtils.h
line17  static C10_UNUSED std::vector<Tensor> expandTensors(const Tensor & self, IOptTensorListRef indices)