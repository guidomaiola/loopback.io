---
lang: en
title: 'API docs: context.binding.toinjectable'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/strongloop/loopback-next/tree/master/packages/context
permalink: /doc/en/lb4/apidocs.context.binding.toinjectable.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/context](./context.md) &gt; [Binding](./context.binding.md) &gt; [toInjectable](./context.binding.toinjectable.md)

## Binding.toInjectable() method

Bind to a class optionally decorated with `@injectable`<!-- -->. Based on the introspection of the class, it calls `toClass/toProvider/toDynamicValue` internally. The current binding key will be preserved (not being overridden by the key inferred from the class or options).

This is similar to [createBindingFromClass()](./context.createbindingfromclass.md) but applies to an existing binding.

<b>Signature:</b>

```typescript
toInjectable(ctor: DynamicValueProviderClass<T> | Constructor<T | Provider<T>>): this;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  ctor | [DynamicValueProviderClass](./context.dynamicvalueproviderclass.md)<!-- -->&lt;T&gt; \| [Constructor](./context.constructor.md)<!-- -->&lt;T \| [Provider](./context.provider.md)<!-- -->&lt;T&gt;&gt; | A class decorated with <code>@injectable</code>. |

<b>Returns:</b>

this

## Example


```ts
@injectable({scope: BindingScope.SINGLETON, tags: {service: 'MyService}})
class MyService {
  // ...
}

const ctx = new Context();
ctx.bind('services.MyService').toInjectable(MyService);

```

