:: BASE_DOC ::

## API

### Link Props

name | type | default | description | required
-- | -- | -- | -- | --
content | String / Slot / Function | - | Typescript：`string | TNode`。[see more ts definition](https://github.com/Tencent/tdesign-vue/blob/develop/src/common.ts) | N
default | String / Slot / Function | - | Typescript：`string | TNode`。[see more ts definition](https://github.com/Tencent/tdesign-vue/blob/develop/src/common.ts) | N
disabled | Boolean | - | make link to be disabled | N
hover | String | underline | hover link style。options：color/underline | N
href | String | - | \- | N
prefixIcon | Slot / Function | - | Typescript：`TNode`。[see more ts definition](https://github.com/Tencent/tdesign-vue/blob/develop/src/common.ts) | N
size | String | medium | options：small/medium/large。Typescript：`SizeEnum`。[see more ts definition](https://github.com/Tencent/tdesign-vue/blob/develop/src/common.ts) | N
suffixIcon | Slot / Function | - | Typescript：`TNode`。[see more ts definition](https://github.com/Tencent/tdesign-vue/blob/develop/src/common.ts) | N
target | String | - | target is an attribute of `<a>` | N
theme | String | default | options：default/primary/danger/warning/success | N
underline | Boolean | - | \- | N
onClick | Function |  | Typescript：`(e: MouseEvent) => void`<br/>click event, it won't trigger when it's disabled | N

### Link Events

name | params | description
-- | -- | --
click | `(e: MouseEvent)` | click event, it won't trigger when it's disabled
