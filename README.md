# WASM WebGL Viewer

Toy viewer to run rust (graphics) programs in the browser using WASM. Currently
draws a triangle to the screen with a user-selectable colour.

Built with the help of https://blog.logrocket.com/implement-webassembly-webgl-viewer-using-rust/.

Subtle things I needed to change in order to get it working:

 - Instead of directly opening the `index.html` file and running into CORS errors,
   run the `web/` directory as a server.  
   I used `python3 -m http.server 5500` to
   get a simple HTTP server going.
 - Use `wasm-pack build --target web --out-dir web/pkg` as the `wasm-pack` build
   command.

##### This project is maintained by [Abhinav Chennubhotla](https://github.com/PhoenixFlame101).
