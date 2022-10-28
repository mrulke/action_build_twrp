<h1 align="center"> Github Actions TWRP Recovery</h1>

---

<p align="center">
	Use Github Action to build TWRP Recovery
</p>

<p align="center">
	This project is a secondary modification (repair) version based on <a href="https://github.com/Pinkdoge/actions_build_recovery">Pinkdoge/actions_build_recovery</a> </p>


## configure

The configuration file is located in the warehouse root directory [Config.json](config.json)

| 名称               | 类型    | 描述                                                         |
| ------------------ | ------- | ------------------------------------------------------------ |
| `twrp_url`     | String  | The source code address used for compilation                                        |
| `twrp_branch`  | String  | The source branch used for compilation                                        |
| `git_username` | String  | Git username                                            |
| `git_email`    | String  | Git mailbox|
| `use_own_dt`   | Boolean | ndicates whether to use the personal device tree<sub>（this item takes effect `true` after the following three items </sub>  |
| `dt_url`           | String  |The address of the device tree you are using<sub>（format: `USER/REPO` ）</sub>                |
| `dt_branch`    | String  | the branch of the device tree you are using                                         |
| `dt_remote`        | String  | You use the device tree's repository<sub>（eg `github/gitlab` ）</sub>               |
| `dt_path`      | String  | Indicates where to save the device tree locally <sub>（eg `device/huawei/kiwi` ）</sub>      |
| `device_code`  | String  | The model code of the model you are going to compile                                     |
| `use_omin_head`  | Boolean  | Indicates whether the  `*.mk` file contains  `omni_` the header<sub>（for example, if your `*.mk` file like  `omni_kiwi.mk` you need to turn this option on）</sub>                                     |
| `use_repair_manifest`  | Boolean | Whether to download the repair environment<sub>（note that this item is the precondition of the last three items. This item takes effect `true` after the following four items) </sub>                              |
| `fix_product`  | Boolean | Indicates whether to fix the problem that the device cannot be found                               |
| `fix_misscom`  | Boolean | Indicates whether to fix `device/qcom/common`  problem                   |
| `fix_busybox`      | Boolean | Indicates whether to fix `busybox` problem 的问题                              |
| `fix_branch`       | String  | Indicate the branch used to fix the above problems<sub>（you generally do not need to modify this item, just replace the corresponding branch of the `Android` version） </sub>                                 |

## Start

After Forkiong this repository, modify [Config.json](config.json)，click Star in the upper right corner to start, you can check the progress in the Star [Worker](../../actions) interface

## compile result
Can be downloaded at [Release](../../releases)
