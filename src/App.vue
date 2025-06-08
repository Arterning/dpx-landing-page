<template>
  <div class="min-h-screen bg-gradient-to-br from-blue-50 to-gray-50">
    <!-- 导航栏 -->
    <nav class="bg-white shadow-sm">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16">
          <div class="flex items-center">
            <div class="flex-shrink-0 flex items-center">
              <svg class="h-8 w-8 text-indigo-600" fill="currentColor" viewBox="0 0 20 20">
                <path d="M10 12a2 2 0 100-4 2 2 0 000 4z" />
                <path fill-rule="evenodd" d="M.458 10C1.732 5.943 5.522 3 10 3s8.268 2.943 9.542 7c-1.274 4.057-5.064 7-9.542 7S1.732 14.057.458 10zM14 10a4 4 0 11-8 0 4 4 0 018 0z" clip-rule="evenodd" />
              </svg>
              <span class="ml-2 text-xl font-bold text-gray-900">DeepParseX</span>
            </div>
          </div>
          <div class="hidden md:ml-6 md:flex md:items-center md:space-x-8">
            <a href="#features" class="text-gray-900 hover:text-indigo-600 px-3 py-2 text-sm font-medium">功能</a>
            <a href="#solutions" class="text-gray-900 hover:text-indigo-600 px-3 py-2 text-sm font-medium">解决方案</a>
            <a href="#pricing" class="text-gray-900 hover:text-indigo-600 px-3 py-2 text-sm font-medium">定价</a>
            <a href="#contact" class="text-gray-900 hover:text-indigo-600 px-3 py-2 text-sm font-medium">联系我们</a>
          </div>
          <div class="flex items-center">
            <a href="#demo" class="ml-8 inline-flex items-center px-4 py-2 border border-transparent text-sm font-medium rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
              申请演示
            </a>
          </div>
        </div>
      </div>
    </nav>

    <!-- 英雄区域 -->
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 md:py-32">
      <div class="lg:grid lg:grid-cols-12 lg:gap-8">
        <div class="sm:text-center md:max-w-2xl md:mx-auto lg:col-span-6 lg:text-left">
          <h1 class="text-4xl tracking-tight font-extrabold text-gray-900 sm:text-5xl md:text-6xl">
            <span class="block">多模态文档智能解析</span>
            <span class="block text-indigo-600">DeepParseX 平台</span>
          </h1>
          <p class="mt-3 text-base text-gray-500 sm:mt-5 sm:text-lg sm:max-w-xl sm:mx-auto md:mt-5 md:text-xl lg:mx-0">
            强大的多模态文档解析与知识管理平台，支持 PDF、Word、Excel、PPT、图片、视频、音频等多种文件格式的智能解析，自动提取关键信息。
          </p>
          <div class="mt-8 sm:max-w-lg sm:mx-auto sm:text-center lg:text-left lg:mx-0">
            <div class="mt-5 sm:mt-8 sm:flex sm:justify-center lg:justify-start">
              <div class="rounded-md shadow">
                <a href="#demo" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 md:py-4 md:text-lg md:px-10">
                  免费试用
                </a>
              </div>
              <div class="mt-3 sm:mt-0 sm:ml-3">
                <a href="#features" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-indigo-700 bg-indigo-100 hover:bg-indigo-200 md:py-4 md:text-lg md:px-10">
                  了解更多
                </a>
              </div>
            </div>
          </div>
        </div>
        <div class="mt-12 relative sm:max-w-lg sm:mx-auto lg:mt-0 lg:max-w-none lg:mx-0 lg:col-span-6 lg:flex lg:items-center">
          <div class="relative mx-auto w-full rounded-lg shadow-lg lg:max-w-md">
            <img class="w-full rounded-lg" src="https://images.unsplash.com/photo-1551434678-e076c223a692?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2850&q=80" alt="DeepParseX 界面展示">
          </div>
        </div>
      </div>
    </div>

    <!-- 功能特点 -->
    <div id="features" class="py-16 bg-white overflow-hidden">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="lg:text-center">
          <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">核心功能</h2>
          <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
            释放非结构化数据的全部价值
          </p>
          <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
            DeepParseX 提供全面的文档解析与知识管理解决方案
          </p>
        </div>

        <div class="mt-20">
          <div class="grid grid-cols-1 gap-12 sm:grid-cols-2 lg:grid-cols-3">
            <div v-for="feature in features" :key="feature.name" class="pt-6">
              <div class="flow-root bg-gray-50 rounded-lg px-6 pb-8">
                <div class="-mt-6">
                  <div>
                    <span class="inline-flex items-center justify-center p-3 bg-indigo-500 rounded-md shadow-lg">
                      <component :is="feature.icon" class="h-6 w-6 text-white" aria-hidden="true" />
                    </span>
                  </div>
                  <h3 class="mt-8 text-lg font-medium text-gray-900 tracking-tight">{{ feature.name }}</h3>
                  <p class="mt-5 text-base text-gray-500">
                    {{ feature.description }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 解决方案 -->
    <div id="solutions" class="py-16 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="lg:text-center">
          <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">行业解决方案</h2>
          <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
            适用于各种业务场景
          </p>
        </div>

        <div class="mt-10">
          <div class="space-y-10 md:space-y-0 md:grid md:grid-cols-2 md:gap-x-8 md:gap-y-10">
            <div v-for="solution in solutions" :key="solution.name" class="relative">
              <div class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                <component :is="solution.icon" class="h-6 w-6" aria-hidden="true" />
              </div>
              <p class="ml-16 text-lg leading-6 font-medium text-gray-900">{{ solution.name }}</p>
              <p class="mt-2 ml-16 text-base text-gray-500">
                {{ solution.description }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 客户评价 -->
    <div class="py-16 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="lg:text-center">
          <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">客户评价</h2>
          <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
            我们的客户怎么说
          </p>
        </div>

        <div class="mt-16 grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
          <div v-for="testimonial in testimonials" :key="testimonial.name" class="pt-6">
            <div class="flow-root bg-gray-50 rounded-lg px-6 pb-8 h-full">
              <div class="-mt-6">
                <div class="flex items-center">
                  <img class="h-12 w-12 rounded-full" :src="testimonial.avatar" :alt="testimonial.name">
                  <div class="ml-4">
                    <h3 class="text-lg font-medium text-gray-900">{{ testimonial.name }}</h3>
                    <p class="text-sm text-gray-500">{{ testimonial.title }}</p>
                  </div>
                </div>
                <p class="mt-5 text-base text-gray-500 italic">
                  "{{ testimonial.quote }}"
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 定价 -->
    <div id="pricing" class="bg-gray-50 py-16">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="lg:text-center">
          <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">定价方案</h2>
          <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
            适合各种规模的企业
          </p>
        </div>

        <div class="mt-16 space-y-12 lg:space-y-0 lg:grid lg:grid-cols-3 lg:gap-x-8">
          <div v-for="tier in pricing.tiers" :key="tier.title" class="relative p-8 bg-white border border-gray-200 rounded-2xl shadow-sm flex flex-col">
            <div class="flex-1">
              <h3 class="text-xl font-semibold text-gray-900">{{ tier.title }}</h3>
              <p class="mt-4 flex items-baseline text-gray-900">
                <span class="text-5xl font-extrabold tracking-tight">¥{{ tier.price }}</span>
                <span class="ml-1 text-xl font-semibold">{{ tier.frequency }}</span>
              </p>
              <p class="mt-6 text-gray-500">{{ tier.description }}</p>

              <ul role="list" class="mt-6 space-y-6">
                <li v-for="feature in tier.features" :key="feature" class="flex">
                  <svg class="flex-shrink-0 w-6 h-6 text-indigo-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="ml-3 text-gray-500">{{ feature }}</span>
                </li>
              </ul>
            </div>

            <div class="mt-8">
              <a :href="tier.href" class="block w-full py-3 px-6 text-center rounded-md border border-transparent bg-indigo-600 text-white font-medium hover:bg-indigo-700">
                {{ tier.buttonText }}
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- CTA -->
    <div id="demo" class="bg-indigo-700">
      <div class="max-w-2xl mx-auto text-center py-16 px-4 sm:py-20 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-extrabold text-white sm:text-4xl">
          <span class="block">准备好体验 DeepParseX 的强大功能了吗？</span>
        </h2>
        <p class="mt-4 text-lg leading-6 text-indigo-200">
          立即申请演示，了解如何利用 AI 技术提升您的数据治理能力。
        </p>
        <a href="#contact" class="mt-8 w-full inline-flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-indigo-600 bg-white hover:bg-indigo-50 sm:w-auto">
          申请演示
        </a>
      </div>
    </div>

    <!-- 联系我们 -->
    <div id="contact" class="bg-white py-16 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto">
        <div class="lg:text-center">
          <h2 class="text-base text-indigo-600 font-semibold tracking-wide uppercase">联系我们</h2>
          <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
            让我们开始对话
          </p>
        </div>

        <div class="mt-10 flex flex-col lg:flex-row lg:space-x-8">
          <div class="lg:w-1/2">
            <form class="space-y-8">
              <div>
                <label for="name" class="block text-sm font-medium text-gray-700">姓名</label>
                <input type="text" id="name" name="name" class="mt-1 block w-full border border-gray-300 rounded-md shadow-sm py-2 px-3 focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
              </div>
              <div>
                <label for="email" class="block text-sm font-medium text-gray-700">邮箱</label>
                <input type="email" id="email" name="email" class="mt-1 block w-full border border-gray-300 rounded-md shadow-sm py-2 px-3 focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
              </div>
              <div>
                <label for="company" class="block text-sm font-medium text-gray-700">公司</label>
                <input type="text" id="company" name="company" class="mt-1 block w-full border border-gray-300 rounded-md shadow-sm py-2 px-3 focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
              </div>
              <div>
                <label for="message" class="block text-sm font-medium text-gray-700">留言</label>
                <textarea id="message" name="message" rows="4" class="mt-1 block w-full border border-gray-300 rounded-md shadow-sm py-2 px-3 focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm"></textarea>
              </div>
              <div>
                <button type="submit" class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                  提交
                </button>
              </div>
            </form>
          </div>
          <div class="lg:w-1/2 mt-8 lg:mt-0">
            <div class="bg-gray-50 p-6 rounded-lg">
              <h3 class="text-lg font-medium text-gray-900">联系方式</h3>
              <div class="mt-4 space-y-4">
                <div class="flex">
                  <svg class="flex-shrink-0 h-6 w-6 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                  </svg>
                  <span class="ml-3 text-gray-500">18874257015</span>
                </div>
                <div class="flex">
                  <svg class="flex-shrink-0 h-6 w-6 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                  </svg>
                  <span class="ml-3 text-gray-500">ning.huang.ridson@gmail.com</span>
                </div>
                <div class="flex">
                  <svg class="flex-shrink-0 h-6 w-6 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                  </svg>
                  <span class="ml-3 text-gray-500">长沙市湘江新区网络安全科技园区</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 页脚 -->
    <footer class="bg-gray-800">
      <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
        <div class="xl:grid xl:grid-cols-3 xl:gap-8">
          <div class="space-y-8 xl:col-span-1">
            <div class="flex items-center">
              <svg class="h-8 w-8 text-indigo-500" fill="currentColor" viewBox="0 0 20 20">
                <path d="M10 12a2 2 0 100-4 2 2 0 000 4z" />
                <path fill-rule="evenodd" d="M.458 10C1.732 5.943 5.522 3 10 3s8.268 2.943 9.542 7c-1.274 4.057-5.064 7-9.542 7S1.732 14.057.458 10zM14 10a4 4 0 11-8 0 4 4 0 018 0z" clip-rule="evenodd" />
              </svg>
              <span class="ml-2 text-xl font-bold text-white">DeepParseX</span>
            </div>
            <p class="text-gray-300 text-base">
              强大的多模态文档解析与知识管理平台，支持多种文件格式的智能解析，自动提取关键信息。
            </p>
          </div>
          <div class="mt-12 grid grid-cols-2 gap-8 xl:mt-0 xl:col-span-2">
            <div class="md:grid md:grid-cols-2 md:gap-8">
              <div>
                <h3 class="text-sm font-semibold text-gray-300 tracking-wider uppercase">产品</h3>
                <ul class="mt-4 space-y-4">
                  <li>
                    <a href="#features" class="text-base text-gray-400 hover:text-white">功能</a>
                  </li>
                  <li>
                    <a href="#pricing" class="text-base text-gray-400 hover:text-white">定价</a>
                  </li>
                  <li>
                    <a href="#demo" class="text-base text-gray-400 hover:text-white">演示</a>
                  </li>
                </ul>
              </div>
              <div class="mt-12 md:mt-0">
                <h3 class="text-sm font-semibold text-gray-300 tracking-wider uppercase">公司</h3>
                <ul class="mt-4 space-y-4">
                  <li>
                    <a href="#" class="text-base text-gray-400 hover:text-white">关于我们</a>
                  </li>
                  <li>
                    <a href="#" class="text-base text-gray-400 hover:text-white">博客</a>
                  </li>
                  <li>
                    <a href="#" class="text-base text-gray-400 hover:text-white">工作机会</a>
                  </li>
                </ul>
              </div>
            </div>
            <div class="md:grid md:grid-cols-2 md:gap-8">
              <div>
                <h3 class="text-sm font-semibold text-gray-300 tracking-wider uppercase">法律</h3>
                <ul class="mt-4 space-y-4">
                  <li>
                    <a href="#" class="text-base text-gray-400 hover:text-white">隐私政策</a>
                  </li>
                  <li>
                    <a href="#" class="text-base text-gray-400 hover:text-white">服务条款</a>
                  </li>
                </ul>
              </div>
              <div class="mt-12 md:mt-0">
                <h3 class="text-sm font-semibold text-gray-300 tracking-wider uppercase">关注我们</h3>
                <div class="mt-4 flex space-x-6">
                  <a href="#" class="text-gray-400 hover:text-white">
                    <span class="sr-only">微信</span>
                    <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                      <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84" />
                    </svg>
                  </a>
                  <a href="#" class="text-gray-400 hover:text-white">
                    <span class="sr-only">GitHub</span>
                    <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                      <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd" />
                    </svg>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="mt-12 border-t border-gray-700 pt-8">
          <p class="text-base text-gray-400 text-center">
            &copy; 2023 DeepParseX 数据科技. 保留所有权利.
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import {
  DocumentTextIcon,
  DatabaseIcon,
  SearchIcon,
  ChartBarIcon,
  CogIcon,
  ShieldCheckIcon,
  AcademicCapIcon,
  BriefcaseIcon,
  ClipboardListIcon,
  LibraryIcon,
  UserGroupIcon
} from '@heroicons/vue/outline'

const features = ref([
  {
    name: '多模态文档解析',
    description: '支持 PDF、Word、Excel、PPT、图片、视频、音频等多种文件格式的智能解析',
    icon: DocumentTextIcon
  },
  {
    name: '关键信息提取',
    description: '自动识别并提取文档中的关键信息，如实体、关系、日期、金额等',
    icon: SearchIcon
  },
  {
    name: '检索增强生成(RAG)',
    description: '构建强大的检索系统，结合生成式 AI 提供精准的问答和内容生成能力',
    icon: DatabaseIcon
  },
  {
    name: '知识图谱构建',
    description: '自动从文档中抽取实体和关系，构建结构化的知识图谱系统',
    icon: ChartBarIcon
  },
  {
    name: '智能数据治理',
    description: '提供完整的数据治理解决方案，包括数据清洗、标准化和质量管理',
    icon: CogIcon
  },
  {
    name: '安全与合规',
    description: '符合行业安全标准，提供数据加密、访问控制和审计日志等功能',
    icon: ShieldCheckIcon
  }
])

const solutions = ref([
  {
    name: '金融文档分析',
    description: '自动化处理金融报告、合同和监管文件，提取关键财务数据和条款',
    icon: BriefcaseIcon
  },
  {
    name: '法律文档处理',
    description: '快速解析法律合同和案例，识别关键条款和法律实体',
    icon: ClipboardListIcon
  },
  {
    name: '医疗记录管理',
    description: '结构化处理医疗报告和病历，支持临床决策和科研分析',
    icon: AcademicCapIcon
  },
  {
    name: '企业知识管理',
    description: '构建企业知识库，实现文档的智能检索和知识共享',
    icon: LibraryIcon
  },
  {
    name: '政府公文处理',
    description: '自动化处理政府公文和档案，提高政务处理效率',
    icon: UserGroupIcon
  }
])

const testimonials = ref([
  {
    name: '张伟',
    title: '某金融机构CTO',
    quote: 'DeepParseX 帮助我们自动化处理了数千份金融报告，节省了数百小时的人工分析时间。',
    avatar: 'https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=256&h=256&q=80'
  },
  {
    name: '李娜',
    title: '某法律科技公司产品总监',
    quote: '知识图谱功能彻底改变了我们处理法律文档的方式，使检索效率提升了300%。',
    avatar: 'https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=256&h=256&q=80'
  },
  {
    name: '王强',
    title: '某医疗集团信息中心主任',
    quote: '多模态解析能力让我们能够统一处理各种格式的医疗记录，极大提升了数据利用率。',
    avatar: 'https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=256&h=256&q=80'
  }
])

const pricing = ref({
  tiers: [
    {
      title: '基础版',
      price: '999',
      frequency: '/月',
      description: '适合小型团队和个人用户',
      features: [
        '每月1000份文档解析',
        '基础信息提取功能',
        '5GB存储空间',
        '标准技术支持',
        '单用户许可'
      ],
      buttonText: '开始试用',
      href: '#demo'
    },
    {
      title: '专业版',
      price: '4999',
      frequency: '/月',
      description: '适合中型企业和部门',
      features: [
        '每月10000份文档解析',
        '高级信息提取功能',
        '50GB存储空间',
        '优先技术支持',
        '5用户许可',
        '基础知识图谱功能'
      ],
      buttonText: '开始试用',
      href: '#demo'
    },
    {
      title: '企业版',
      price: '19999',
      frequency: '/月',
      description: '适合大型企业和机构',
      features: [
        '无限制文档解析',
        '全部高级功能',
        '1TB存储空间',
        '24/7专属技术支持',
        '多用户许可',
        '完整知识图谱系统',
        '定制开发支持'
      ],
      buttonText: '联系我们',
      href: '#contact'
    }
  ]
})
</script>

<style>
/* 可以在这里添加自定义样式 */
</style>