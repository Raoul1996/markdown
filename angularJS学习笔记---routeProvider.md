# angularJS学习笔记---routeProvider() #

9/5/2016 9:51:51 PM 

*eidtor:raoul*

----------

**angularJS只的路由(routeProvider)使用语法:**
	var bookstoreApp = angular.module('bookstoreApp',[
		'ngRoute','ngAnimate','bookStoreCtrls','bookStoreFilters','bookStoreServices','bookStoreDirectives'
	]);//注明bookStoreApp启动所需要的依赖

	bookstoreApp.config(function($routeProvider){
		$routeProvider.when('/hello',{
			templateUrl:'tpls/hello.html',
			controller:'HelloCtrl'
		}).when('/list',{
			templateUrl:'tpls/list.html',
			controller:'BooklistCtrl'
		}).otherwise({
			redirectTo: '/hello'
		})
	});