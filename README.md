# CubeSpec Fine Steering Mirror benchmark dataset

This benchmark dataset contains input–output data from the CubeSpec Fine Steering Mirror, a multi-input multi-output high-precision control platform used in a small satellite. Voltages applied to three piezo-actuators serve as inputs, while the mirror displacements measured at three non-collocated reference points serve as outputs.

The excitation signals are orthogonal random-phase multisines spanning a wide frequency range, and are applied at three different amplitude levels.  The system behaves mostly linearly, but the presence of hysteresis in the piezo-actuators introduces dynamic nonlinearities, making the dataset well-suited for benchmarking nonlinear identification methods.

Further details about the dataset and its experimental setup can be found [here](https://lirias.kuleuven.be/retrieve/775145).

## Baseline model

A baseline implementation for a linear model is included.  It uses the [`freq-statespace`](https://github.com/merijnfloren/freq-statespace) Python package to fit a 28th-order state-space model.  While the model achieves a good fit, the residuals do not match the experimental noise floor, indicating that more advanced nonlinear models could further improve performance.

## Citation

If you use this dataset, please cite:

```bibtex
@article{floren2024data,
  title={Data-driven state-space identification and nonlinearity assessment of the CubeSpec Fine Steering Mirror},
  author={Floren, Merijn and Peri, Leonardo and De Maeyer, Jeroen and De Munter, Wim and Vandepitte, Dirk and No{\"e}l, Jean-Philippe},
  journal={ISMA-USD2024},
  year={2024}
}
```
