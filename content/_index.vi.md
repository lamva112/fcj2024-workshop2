---
title : "Deploy Spring Boot applications onto AWS ECS Fargate using AWS CDK."
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---

# Sử dụng AWS CDK để triển khai dịch vụ Spring Boot trên AWS ECS Fargate

#### Tổng quan

Trong wokshop này, chúng ta sẽ tạo ra một microservices bằng Java 21, sử dụng framework Spring Boot V3 và các container Docker, xây dựng một ứng dụng backend để tương tác với các tài nguyên của Amazon Web Services (AWS). Các tài nguyên này sẽ được tạo trong AWS bằng cách sử dụng AWS Cloud Development Kit (CDK) V2, một cách hiện đại để mô hình hóa và cấu hình cơ sở hạ tầng trong AWS. AWS CDK là một trong những công cụ tốt nhất cho việc quản lý cơ sở hạ tầng dưới dạng mã, hay còn gọi là IaC (Infrastructure as Code), trên AWS.

![Architect](/images/architect.svg?featherlight=false&width=80pc)