<template>
    <div class="p-5">
        <div>
            <div v-if="$page.props.user.permissions.includes('read articles')">
                <button
                    type="button"
                    class="bg-green-500 text-white rounded-md p-3 mb-2 w-1/5"
                >
                    Read article
                </button>
            </div>

            <div v-if="$page.props.user.permissions.includes('write articles')">
                <button
                    type="button"
                    class="bg-blue-500 text-white rounded-md p-3 mb-2 w-1/5"
                >
                    Write article
                </button>
            </div>

            <div v-if="$page.props.user.permissions.includes('edit articles')">
                <button
                    type="button"
                    class="bg-yellow-500 text-white rounded-md p-3 mb-2 w-1/5"
                >
                    Edit article
                </button>
            </div>

            <div
                v-if="$page.props.user.permissions.includes('delete articles')"
            >
                <button
                    type="button"
                    class="bg-red-500 text-white rounded-md p-3 mb-2 w-1/5"
                >
                    Delete article
                </button>
            </div>
        </div>

        <div class="bg-green-300 mt-3 rounded-md p-2">
            {{ $page.props }}
        </div>
    </div>
</template>
