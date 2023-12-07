## John Ahn님 Nest.JS 강의 클론코딩

Nest.JS 강의를 찾아보던 차, 무료로 제공해주시는 강의가 있어 스터디 할 수 있었습니다.
감사합니다.
[![john ahn님 유튜브 채널](https://github.com/pioneer2077/nextjs_practice/assets/134494401/6d49d091-48c0-4f3b-9fd6-4d8ea6054958)](https://www.youtube.com/@johnahn.)
(클릭하시면 유튜브 채널로 이동합니다!)

### 목차

1. Nest.JS ?
2. 프로젝트 구조
3. 어려웠던 점
4. 알게된 점
5. 회고

## Nest.JS ?

Nest.JS는 효율적이고 안정적이며 확장 가능한 서버측 애플리케이션을 구축하기 위한 Node.js 프레임워크입니다.
Express 위에서 작동하죠.
<br />
<br />
따라서 Express의 라우팅 및 미들웨어 기능을 활용하면서,
Nest.JS의 추가적인 기능과 프레임워크로서의 구조를 사용할 수 있어요.
<br />
<br />
adidas, BMW, Red Hat 등 많은 대기업에서 사용중인
<br />
백엔드 프레임워크에요.
<br />

React components implement a `render()` method that takes input data and returns what to display. This example uses an XML-like syntax called JSX. Input data that is passed into the component can be accessed by `render()` via `this.props`.

```jsx
class HelloMessage extends React.Component {
  render() {
    return <div>Hello {this.props.name}</div>;
  }
}

root.render(<HelloMessage name="Taylor" />);
```

## Declarative

React makes it painless to create interactive UIs. Design simple views for each state in your application, and React will efficiently update and render just the right components when your data changes.

A paragraph with _emphasis_ and **strong importance**.

> A block quote with ~strikethrough~ and a URL: https://reactjs.org.

- Lists
- [ ] todo
- [x] done

## Component-Based

Build encapsulated components that manage their own state, then compose them to make complex UIs.

Since component logic is written in JavaScript instead of templates, you can easily pass rich data through your app and keep state out of the DOM.

## Learn Once, Write Anywhere

We don’t make assumptions about the rest of your technology stack, so you can develop new features in React without rewriting existing code.

React can also render on the server using Node and power mobile apps using React Native.

![React Office desk](https://images.unsplash.com/photo-1633356122102-3fe601e05bd2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80)

> The most important addition in React 18 is something we hope you never have to think about: concurrency. We think this is largely true for application developers, though the story may be a bit more complicated for library maintainers.

Concurrency is not a feature, per se. It’s a new behind-the-scenes mechanism that enables React to prepare multiple versions of your UI at the same time. You can think of concurrency as an implementation detail — it’s valuable because of the features that it unlocks. React uses sophisticated techniques in its internal implementation, like priority queues and multiple buffering. But you won’t see those concepts anywhere in our public APIs.

When we design APIs, we try to hide implementation details from developers. As a React developer, you focus on what you want the user experience to look like, and React handles how to deliver that experience. So we don’t expect React developers to know how concurrency works under the hood.

However, Concurrent React is more important than a typical implementation detail — it’s a foundational update to React’s core rendering model. So while it’s not super important to know how concurrency works, it may be worth knowing what it is at a high level.

A key property of Concurrent React is that rendering is interruptible. When you first upgrade to React 18, before adding any concurrent features, updates are rendered the same as in previous versions of React — in a single, uninterrupted, synchronous transaction. With synchronous rendering, once an update starts rendering, nothing can interrupt it until the user can see the result on screen.

In a concurrent render, this is not always the case. React may start rendering an update, pause in the middle, then continue later. It may even abandon an in-progress render altogether. React guarantees that the UI will appear consistent even if a render is interrupted. To do this, it waits to perform DOM mutations until the end, once the entire tree has been evaluated. With this capability, React can prepare new screens in the background without blocking the main thread. This means the UI can respond immediately to user input even if it’s in the middle of a large rendering task, creating a fluid user experience.

Another example is reusable state. Concurrent React can remove sections of the UI from the screen, then add them back later while reusing the previous state. For example, when a user tabs away from a screen and back, React should be able to restore the previous screen in the same state it was in before. In an upcoming minor, we’re planning to add a new component called `<Offscreen>` that implements this pattern. Similarly, you’ll be able to use Offscreen to prepare new UI in the background so that it’s ready before the user reveals it.

Concurrent rendering is a powerful new tool in React and most of our new features are built to take advantage of it, including Suspense, transitions, and streaming server rendering. But React 18 is just the beginning of what we aim to build on this new foundation.
