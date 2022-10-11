---
layout: home
title: Preact
show_title: false
toc: false
description: 'React 的 3kb 轻量化方案，拥有更现代化的 API。'
---

<jumbotron>
    <h1>
        <logo height="1.5em" title="Preact" text inverted>Preact</logo>
    </h1>
    <p class="tagline">React 的 3kb 轻量化方案，拥有更现代化的 API</p>
    <p class="intro-buttons">
        <a href="/guide/v10/getting-started" class="btn primary">现在开始</a>
        <a href="/guide/v10/switching-to-preact" class="btn secondary">切换到 Preact</a>
    </p>
</jumbotron>

```jsx
function Counter() {
  const [value, setValue] = useState(0);

  return (
    <>
      <div>Counter: {value}</div>
      <button onClick={() => setValue(value + 1)}>Increment</button>
      <button onClick={() => setValue(value - 1)}>Decrement</button>
    </>
  )
}
```

<section class="sponsors">
  <p>由以下组织 <a href="https://opencollective.com/preact">提供赞助：</a></p>
  <sponsors></sponsors>
</section>

<section class="home-top">
    <h1>与众不同的库</h1>
</section>

<section class="home-section">
  <img src="/assets/home/metal.svg" alt="metal" loading="lazy" width="54" height="54">

  <div>
    <h2>更接近于真实 DOM</h2>
    <p>
      Preact 在 DOM 之上提供的虚拟 DOM 抽象可能是目前最简洁的。
      它构建在稳定的平台特性之上，注册真实的事件处理程序，并且可以很好地与其他库一起使用。
    </p>
    <p>
      Preact 可以直接在浏览器中使用，不需要任何转换步骤。
    </p>
  </div>
</section>

<section class="home-section">
  <img src="/assets/home/size.svg" alt="size" loading="lazy" width="54" height="54">

  <div>
    <h2>轻量级</h2>
    <p>
      大多数 UI 框架的体积都大到成为了应用程序 JavaScript 包体积的主要部分。
      Preact 则不同：它足够小，而 <em>你的代码</em> 才是你应用程序中的主要部分。
    </p>
    <p>
      这意味着客户端会下载、解析和执行更少的 JavaScript - 留出更多时间给你的业务逻辑代码，因此你可以专注构建称心如意的应用而不用跟框架做太多无谓的交互。
    </p>
  </div>
</section>

<section class="home-section">
  <img src="/assets/home/performance.svg" alt="performance" loading="lazy" width="54" height="54">

  <div>
    <h2>卓越的性能</h2>
    <p>
      Preact 非常快，并且不只是因为其体积优势。它是业界目前最快的虚拟 DOM 库之一，得益于一个简洁且可预测的 diff 算法实现。
    </p>
    <p>
      我们会自动地将更新进行统一批处理，并把 Preact 在性能方面做到极致。我们与浏览器工程师紧密合作，以尽可能提高 Preact 的性能。
    </p>
  </div>
</section>

<section class="home-section">
  <img src="/assets/home/portable.svg" alt="portable" loading="lazy" width="54" height="54">

  <div>
    <h2>可移植 &amp; 可嵌入</h2>
    <p>
      Preact 的微小体积意味着你可以将这套虚拟 DOM 组件的机制更容易地迁移到任何一个可能的平台中。
    </p>
    <p>
      可以使用 Preact 构建应用程序的各个部分时，不需要进行复杂的集成。也可以将 Preact 嵌入到小部件中，并应用与构建完整应用程序相同的工具和技术。
    </p>
  </div>
</section>

<section class="home-section">
  <img src="/assets/home/productive.svg" alt="productive" loading="lazy" width="54" height="54">

  <div>
    <h2>立刻具备生产力</h2>
    <p>
      轻量级更有趣的优势是可以使你不必牺牲生产力来达到目标。Preact 能帮你立刻提升效率。甚至还有一些额外的功能:
    </p>
    <ul>
      <li><code>props</code>、<code>state</code> 和 <code>context</code> 将被传入到 <code>render()</code> 中</li>
      <li>可以使用标准的 HTML attributes 比如 <code>class</code> 和 <code>for</code></li>
    </ul>
  </div>
</section>

<section class="home-section">
  <img src="/assets/home/compatible.svg" alt="compatible" loading="lazy" width="54" height="54">

  <div>
    <h2>生态兼容</h2>
    <p>
      虚拟 DOM 组件使你可以很方便的重用和组合 —— 小到按钮，大到数据提供来源。
      Preact 的设计使你可以无缝地使用 React 生态系统中可用的无数组件。
    </p>
    <p>
      只需添加一个 <a href="/guide/v10/switching-to-preact#how-to-alias-preact-compat">preact/compat</a> 别名给打包工具，就可以提供一个兼容层，
      即使最复杂的 React 组件也可以过继使用。
    </p>
  </div>
</section>

<section class="home-top">
    <h1>「 码 」上见分晓！</h1>
</section>

<section class="home-split">
    <div>
        <h2>Todo List</h2>
        <pre><code class="lang-jsx">
export default class TodoList extends Component {
    state = { todos: [], text: '' };
    setText = e =&gt; {
        this.setState({ text: e.target.value });
    };
    addTodo = () =&gt; {
        let { todos, text } = this.state;
        todos = todos.concat({ text });
        this.setState({ todos, text: '' });
    };
    render({ }, { todos, text }) {
        return (
            &lt;form onSubmit={this.addTodo} action="javascript:"&gt;
                &lt;label&gt;
                  &lt;span&gt;Add Todo&lt;/span&gt;
                  &lt;input value={text} onInput={this.setText} /&gt;
                &lt;/label&gt;
                &lt;button type="submit"&gt;Add&lt;/button&gt;
                &lt;ul&gt;
                    { todos.map( todo =&gt; (
                        &lt;li&gt;{todo.text}&lt;/li&gt;
                    )) }
                &lt;/ul&gt;
            &lt;/form&gt;
        );
    }
}
        </code></pre>
    </div>
    <div>
        <h2>Running Example</h2>
        <pre repl="false"><code class="lang-jsx">
import TodoList from './todo-list';

render(&lt;TodoList /&gt;, document.body);
        </code></pre>
        <div class="home-demo">
            <todo-list></todo-list>
        </div>
    </div>
</section>

<section class="home-split">
    <div>
        <h2>Fetch GitHub Stars</h2>
        <pre><code class="lang-jsx">
export default class Stars extends Component {
    async componentDidMount() {
        let stars = await githubStars(this.props.repo);
        this.setState({ stars });
    }
    render({ repo }, { stars=0 }) {
        let url = `https://github.com/${repo}`;
        return (
            &lt;a href={url} class="stars"&gt;
                ⭐️ {stars} Stars
            &lt;/a&gt;
        );
    }
}
        </code></pre>
    </div>
    <div>
        <h2>Running Example</h2>
        <pre repl="false"><code class="lang-jsx">
import Stars from './stars';

render(
    &lt;Stars repo="preactjs/preact" /&gt;,
    document.body
);
        </code></pre>
        <div class="home-demo">
            <github-stars simple user="preactjs" repo="preact"></github-stars>
        </div>
    </div>
</section>

<section class="home-top">
    <h1>准备好一试了吗？</h1>
</section>

<section style="text-align:center;">
    <p>
        如果你曾有 React 相关的经验，我们为你准备了单独的指南。
        <br>
        选择最适合你的指南吧！
    </p>
    <p>
        <a href="/guide/v10/getting-started" class="btn primary">现在开始</a>
        <a href="/guide/v10/switching-to-preact" class="btn secondary">切换到 Preact</a>
    </p>
</section>
