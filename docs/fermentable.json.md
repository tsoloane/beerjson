The schema defines the following types:

## FermentableBase

FermentableBase provides unique properties to identify individual records of fermentable ingredients

`FermentableBase` type: `object`

### Properties

|                 | Type                                                                                  | Description | Required           |
| --------------- | ------------------------------------------------------------------------------------- | ----------- | ------------------ |
| **name**        | string                                                                                |             | :white_check_mark: |
| **type**        | 'dry extract' , 'extract' , 'grain' , 'sugar' , 'fruit' , 'juice' , 'honey' , 'other' |             | :white_check_mark: |
| **origin**      | string                                                                                |             |                    |
| **supplier**    | string                                                                                |             |                    |
| **grain_group** | 'base' , 'caramel' , 'flaked' , 'roasted' , 'specialty' , 'smoked' , 'adjunct'        |             |                    |
| **yield**       | object                                                                                |             | :white_check_mark: |
| **color**       | [ColorType](measureable_units.json.md#colortype)                                      |             | :white_check_mark: |

## FermentableType

FermentableType collects the attributes of a fermentable ingredient to store as record information

`FermentableType` type: `object`

Parent: [FermentableBase](#fermentablebase)

### Properties

|                            | Type                                                               | Description | Required |
| -------------------------- | ------------------------------------------------------------------ | ----------- | -------- |
| **notes**                  | string                                                             |             |          |
| **moisture**               | [PercentType](measureable_units.json.md#percenttype)               |             |          |
| **alpha_amylase**          | number                                                             |             |          |
| **diastatic_power**        | [DiastaticPowerType](measureable_units.json.md#diastaticpowertype) |             |          |
| **protein**                | [PercentType](measureable_units.json.md#percenttype)               |             |          |
| **soluble_nitrogen_ratio** | number                                                             |             |          |
| **max_in_batch**           | [PercentType](measureable_units.json.md#percenttype)               |             |          |
| **recommend_mash**         | boolean                                                            |             |          |
| **inventory**              | object                                                             |             |          |

## FermentableAdditionType

FermentableAdditionType collects the attributes of each fermentable ingredient for use in a recipe fermentable bill

`FermentableAdditionType` type: `object`

Parent: [FermentableBase](#fermentablebase)

### Properties

|            | Type      | Description                                                                                                                     | Required |
| ---------- | --------- | ------------------------------------------------------------------------------------------------------------------------------- | -------- |
| **timing** | object    | The timing object fully describes the timing of an addition with options for basis on time, gravity, or pH at any process step. |          |
| **amount** | undefined |                                                                                                                                 |          |
