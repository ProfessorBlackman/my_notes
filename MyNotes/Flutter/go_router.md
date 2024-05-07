## Definition:
- for enhanced routing in flutter

## Setup
```dart
MaterialApp.router(
  routerConfig: _router,
  title: "Go router",
);

```
- Create a router class with the below method:
```dart
final GoRouter _router = GoRouter(
  routes: [
    GoRoute(
      path: "/",
      builder: (context, state) => const HomePage(),
    ),
    GoRoute(
      path: "/settings",
      builder: (context, state) => const SettingsPage(),
    )
  ],
);

```

## How to navigate b/n routes
```dart
child: ElevatedButton(
  onPressed: () => context.go("/settings"),
  child: const Text("Go to Settings page"),
),

```
- When someone taps this button, they'll be routed to the settings page. 
- This is done by `context.go("/settings")`
## Subroutes
- If you need deeply nested routes, then you have to type the whole route with the leading `/` every time. You can avoid this with subroutes
- Subroutes also improves organization.
```dart
final GoRouter _router = GoRouter(
  routes: [
    GoRoute(
      path: "/",
      builder: (context, state) => const HomePage(),
      routes: [
        GoRoute(
          path: "settings",
          builder: (context, state) => const SettingsPage(),
        )
      ],
    ),
  ],
);

```

## Route parameters
- For passing data accross routes
```dart
final GoRouter _router = GoRouter(
  routes: [
    GoRoute(
      path: "/",
      builder: (context, state) => const HomePage(),
      routes: [
        GoRoute(
          path: "settings/:name",
          builder: (context, state) => SettingsPage(
            name: state.params["name"]!,
          ),
        )
      ],
    ),
  ],
);

```
- To recieve the param:
```dart
class SettingsPage extends StatelessWidget {
  final String name;

  const SettingsPage({super.key, required this.name});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        automaticallyImplyLeading: true,
        title: Text(name),
      ),
      body: Center(
        child: ElevatedButton(
          onPressed: () => context.go("/"),
          child: const Text("Go to home page"),
        ),
      ),
    );
  }
}

```

## Named routes:
- named routes can be used to avoid writing routes manually
```dart
final GoRouter _router = GoRouter(
  routes: [
    GoRoute(
      name: "home",
      path: "/",
      builder: (context, state) => const HomePage(),
      routes: [
        GoRoute(
          name: "settings",
          path: "settings/:name",
          builder: (context, state) => SettingsPage(
            name: state.params["name"]!,
          ),
        )
      ],
    ),
  ],
);


```
- passing params to a named route has to be done as below:
```dart
child: ElevatedButton(
  onPressed: () => context.goNamed(
    "settings",
     params: {"name": "codemagic"},
     ),
  child: const Text("Go to Settings page"),
),

```

## Query params
- The best thing about `queryParams` is that you don’t have to explicitly define them in your route path and can easily access them using the `state.queryParams` method.
```dart
child: ElevatedButton(
  onPressed: () => context.goNamed("settings", params: {
    "name": "codemagic"
  }, queryParams: {
    "email": "example@gmail.com",
    "age": "25",
    "place": "India"
    }),
    child: const Text("Go to Settings page"),
),

```
- To access them:
```dart
GoRoute(
  name: "settings",
  path: "settings/:name",
  builder: (context, state) {
    state.queryParams.forEach(
      (key, value) {
        print("$key:$value");
       },
     );
   return SettingsPage(
     name: state.params["name"]!,
   );
 },
)

```

## 404 errors
- Define an error screen and add it to the router configs
```dart
final GoRouter _router = GoRouter(
  errorBuilder: (context, state) => const ErrorScreen(),
);

```

## Redirects
- Sometimes, you want to programmatically navigate your user from one page to another based on certain logic. You can enable that feature using redirects in `go_router`. You can define a redirect for every path and a global redirect for all pages.
```dart
final GoRouter _router = GoRouter(
  routes: [
    GoRoute(
      name: "home",
      path: "/",
      builder: (context, state) => const HomePage(),
      redirect: (context, state) {
        if (userIsNotLoggedIn){
          return "/login"
        }
        return "/"
      },
    ),
  ],
  errorBuilder: (context, state) => const ErrorScreen(),
);

```