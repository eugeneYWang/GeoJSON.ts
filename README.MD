# GeoJSON.ts, a GeoJSON Parser in TypeScript

Turn your geo data info GeoJSON, as a parser, innovated by @caseycesari/GeoJSON.js in javascript. @EugeneYWang/GeoJSON.ts is that library in TS.

### The reason to create this repo

Usually, an existed NPM package can just be used in TypeScript if a type definition file with the same name of that package is also installed. So why should I refactor that library into this typescript one? The reason is that the type definition named as GeoJSON has been occupied as the type definition of GeoJSON standard specification. Therefore, no one could contribute a type definition in TypeDefinition for @caseycesari/GeoJSON.js.

### Installation

If you are looking for a NPM package in javascript, @caseycefari/GeoJSON.js will be your best fit. If you want to use this in typescript environment (e.g. Angular, React working in Typescript, etc), you can feel free to download `geojson.ts` or `git clone https://github.com/eugeneYWang/GeoJSON.ts`. 

### Use case

```
const geo = new GeoJSON();
const data = {
  name: "Location A",
  category: "Store",
  street: "Market",
  lat: 39.9,
  lng: -75.3
};

const data1 = {
  name: "Location B",
  category: "Store",
  street: "Market",
  lat: 39.984,
  lng: -75.343
};

const res = geo.parse(data, { Point: ["lat", "lng"] });
const res1 = geo.parse(data1, { Point: ["lat", "lng"] });

console.log(res); // a geojson object named Location A

console.log(res1); // a geojson object named Location B

// end
```

### More use cases

You can see more usage on [Casey's README](https://github.com/caseycesari/GeoJSON.js/blob/master/README.md) since the only one more step by using this typescript version is to do `const geojsonTS = new GeoJSON();` first. 

### Welcome to throw your ideas to me!

If you have any idea to make this library better, please feel free to drop a post on issue and "at" @EugeneYWang. If it is a new feature request, you may also want to drop a post to @caseycesari/GeoJSON.js. If I make any new feature to this library, I will contribute its codes to @caseycesari/GeoJSON.js

I am wondering if I need to occupy a spot at NPM, but I am not sure if I have to contribute a javscript version. I do not want to do is to take place of GeoJSON.js, so if NPM does not accept Typescript at all, I might not make it in NPM. If you have any idea to spread this Typescript library easily without hurting GeoJSON.js, please let me know! I will be willing to make this more accessible! 