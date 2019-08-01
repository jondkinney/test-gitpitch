---
### This code presentation works
@size[0.8em](Common components can be packaged up to be reused)

```jsx
const Layout = ({ children }) => {
  return (
    <div>
      <Header>
      {children}
      <Footer>
    </div>
  );
};

export default Layout;
```
@[4](Header shows highlighted here properly because the forward slash is absent in what should be a self closing tag. It should be `<Header />` )


---
### This one does not
@size[0.8em](Common components can be packaged up to be reused)

```jsx
const Layout = ({ children }) => {
  return (
    <div>
      <Header />
      {children}
      <Footer />
    </div>
  );
};

export default Layout;
```
@[4](This breaks when trying to highlight line 4 (or 6 if you try that one) and it jumps the line numbers weird, too. It seems like some of the code isn't being properly escaped or something. If you re-watch the video you will see it there, too.)
