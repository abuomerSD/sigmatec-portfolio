<template>
  <div class="flex justify-center">
    <div class="w-11/12">
      <div class="flex justify-center">
        <h1 class="text-2xl cairo text-blue-900">المنتجات</h1>
      </div>
      <div class="md:grid md:grid-cols-3 md:gap-2">
        <div
          class="rounded bg-amber-300 h-[400px]"
          v-for="(category, index) in categories"
          :key="index"
        >
          <img
            class="w-[400px] h-[200px] rounded border-2 border-blue-900"
            :src="category.image"
            alt="image"
          />
          <h3 class="cairo">{{ category.name }}</h3>
          <p class="overflow-y-auto">{{ category.info }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const categories = ref([
  {
    name: "ماركة هيونداي الكورية",
    image: "/src/assets/images/products/hyundai-products.jpg",
    info: "ماركة هيونداي الكورية تعد من الشركات الرائدة عالمياً في مجال المعدات الكهربائية الصناعية وقطع الغيار. تتميز منتجاتها بالاعتمادية والجودة العالية، وتشمل محركات كهربائية، مفاتيح كهربائية، قواطع، ووحدات التحكم الصناعية. تُستخدم في المصانع والمنشآت الصناعية لتوفير أداء مستقر وفعال، وتضمن ماركة هيونداي تقليل الأعطال والصيانة المتكررة بفضل تكنولوجيا متقدمة ومعايير صارمة للجودة.",
  },
  {
    name: "ماركة دلتا التايوانية",
    image: "/src/assets/images/products/delta-products.jpg",
    info: "ماركة دلتا التايوانية تُعد من الشركات الرائدة عالمياً في مجال معدات الكهرباء الصناعية وأنظمة التحكم الآلي. تقدم دلتا مجموعة واسعة من المنتجات عالية الجودة مثل محركات التحكم، محولات الطاقة، وحدات التحكم الصناعية (PLC)، والمشغلات الكهربائية. تشتهر دلتا بالموثوقية والأداء العالي، مما يجعلها خيارًا مثاليًا للمصانع والمنشآت الصناعية الراغبة في تحقيق كفاءة تشغيلية عالية وتقليل الأعطال.",
  },
  {
    name: "مكونات اللوحات الكهربائية",
    image: "/src/assets/images/products/accessories.jpg",
    info: "كل ما يخص الكهرباء الصناعية من الريليهات و الساعات الحرارية و غيرها",
  },
]);
</script>

<style></style>
