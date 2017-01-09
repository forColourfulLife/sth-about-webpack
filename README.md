# sth-about-webpack
记录在使用webpack过程中碰到的一些问题

1.在使用code-splitting时，在webpack.config.js里设置output.publicPath的值，代码分割后会放在publickPath指定目录里。默认名字是[id].js,如果要改名字的话，需要设置output.chunkFilename，然后在require.ensure([],function(require){}, chunkName)方法里传入chunkName与配置项output.chunkFilename进行匹配。如果静态资源放置在别的域名下，则必须设置output.crossOriginLoading允许跨域。
